---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/001-react-fundamentals/004-props/002-destructuring-props/","tags":["programming","ReactJS","javascript","props"],"created":"2025-07-13T15:25:33.902+08:00"}
---

---
We can immediately destructure `props` by naming the argument in the _component_ the __same name__ as the `prop` being passed.

and putting them inside __curly braces__ `{ }`
> [!example]
```js
function Pizza({ pizzaObj }) {
  if (pizzaObj.soldOut) return null;
  return (
    <li className="pizza">
      <img src={pizzaObj.photoName} alt={pizzaObj.name} />
      <div>
        <h3>{pizzaObj.name}</h3>
        <p>{pizzaObj.ingredients}</p>
        <span>{pizzaObj.price + 3}</span>
      </div>
    </li>
  );
}
```

##### Multiple `props`:
```js
function Order({ closeHour, openHour }) {
  return (
    <div className="order">
      <p>
        We're open from {openHour}:00 to {closeHour}:00. Come visit us or order
        online.
      </p>
      <button className="btn">Order</button>
    </div>
  );
}
```