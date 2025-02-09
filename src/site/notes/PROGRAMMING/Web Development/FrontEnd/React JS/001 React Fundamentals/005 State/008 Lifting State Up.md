---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/005-state/008-lifting-state-up/","tags":["programming","ReactJS","javascript","state","liftingup"],"created":"2025-02-08T16:24:58.788+08:00"}
---


> [!caution] Problem:
> Sharing `state` with __SIBLING__ `component`
> ___`data` can only flow down and not sideways___
> ###### Solution:
> Lifting a `useState()` up the component tree.

### Example scenario:
For example, there's a _parent component_ "`Checkout`" with __child components__: `Total` (which shows the total value of the item) and `Promotions` (that handles the submission or form of coupon codes).

Now if we enter a coupon code in the `Promotions component`, the value should change after applying the coupon code.

We can't change the value inside `Total component` because we can't pass or update the state from `Promotions` to `Total` since they're __siblings components__ and we CAN'T ___pass data sideways in react___, __only downward__ to the `component` tree.

![Pasted image 20250208170321.png](/img/user/Misc/attachments/Pasted%20image%2020250208170321.png)

- So, now we __UPLIFT__ the `const [coupons, setCoupons] = useState("")` to the parent component of both `Promotions` and `Total` which is the `"Checkout" component`.
- and then, we pass the `"coupon" state` as  a __prop__ to the `Total component` to update the displayed __Total value__
- and the `"setCoupons" state function` as a __prop__ to `Promotions component` to update the `"coupons" state` .

---

### Example:

```jsx
// ...

export default function App() {
  const [items, setItems] = useState([]);

  function handleAddItems(item) {
    setItems(items => [...items, item]);
  }

  return (
  <div className="app">
    <Logo />
    <Form onAddItems={handleAddItems}/>
    <PackingList items={ items }/>
    <Stats />
  </div>
  );
}

function Form({ onAddItems }) {
  const [description, setDescription] = useState("");
  const [quantity, setQuantity] = useState(5);

  function handleSubmit(e) {
    e.preventDefault();

    // to prevent from submitting, if it's empty
    if (!description) return;

    // Object or JSON data
    const newItem = { description, quantity, packed: false,
      id: Date.now()};
    console.log(newItem);

    onAddItems(newItem);

    // Reset the State(s)
    setDescription('');
    setQuantity(1);
}
  return (
    <form className="add-form" onSubmit={handleSubmit}>
      <h3>What do you need for your 😍 trip?</h3>

      <select value={quantity} onChange={(e) => setQuantity(Number(e.target.value))}>
        {/* creating an empty array (which is 20 items), "i + 1" so that it would start at 1 and not 0 */}
        {Array.from({length: 20}, (_, i) => i + 1).
        map(num=><option value={num} key={num}>{num}</option>)}
      </select>

      {/* Type > setDescription's State(description) > put it as value */}
      <input type='text' placeholder="Item..." value={description} onChange={(e) => setDescription(e.target.value)}/>
      <button>Add</button>
    </form>
  );
}

function PackingList({ items }) {
  return (
    <div className="list">
      <ul>
        {/* Iterate through the Items */}
        {items.map(item=>
          <Item item={item} key={item.id} />
        )}
      </ul>
    </div>
  );
}

function Item({ item }) {
  return (
    <li>
      {/* Cross-off "packed" items */}
      <span style={item.packed ? {textDecoration: "line-through"}: {}}>
        {item.quantity} {item.description}
      </span>
      <button>❌</button>
    </li>
  );
}

function Stats() {
  return (
    <footer className="stats">
      <em>You have X items on your list, and you already packed X (X%)</em>
    </footer>
  );
}
```
- originally, the `[items, setItems] state` was inside `Form() component`

