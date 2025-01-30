---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/003-jsx/006-conditional-rendering-with-multiple-returns/","tags":["programming","ReactJS","javascript","jsx"],"created":"2025-01-05T00:55:32.819+08:00"}
---

---

> [!abstract] 
> There's nothing stopping us from adding multiple `return` keyword __based on some condition__.

>[!example] Examples:

```js
function Footer() {
  const hour = new Date().getHours();
  const openHour = 12;
  const closeHour = 20;
  const isOpen = hour >= openHour && hour <= closeHour;
  console.log(isOpen);
   return (
    <footer className="footer">

      {/* Conditional Rendering with Ternaries: */}
      {isOpen ? (
        <div className="order">
          <p>We're open until {closeHour}:00. Come visit us or order online.</p>
          <button className="btn">Order</button>
        </div>
      ) : (
        <p>
          We're happy to welcome you between {openHour}:00 and {closeHour}:00.
        </p>
      )}
    </footer>
  );
}
```

```js
function Pizza(props) {
  console.log(props);

  if (props.pizzaObj.soldOut) return null;
  return (
    <li className="pizza">
      <img src={props.pizzaObj.photoName} alt={props.pizzaObj.name} />
      <div>
        <h3>{props.pizzaObj.name}</h3>
        <p>{props.pizzaObj.ingredients}</p>
        <span>{props.pizzaObj.price + 3}</span>
      </div>
    </li>
  );
}
```

