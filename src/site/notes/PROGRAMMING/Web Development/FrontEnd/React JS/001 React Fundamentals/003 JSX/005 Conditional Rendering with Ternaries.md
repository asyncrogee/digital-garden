---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/003-jsx/005-conditional-rendering-with-ternaries/","tags":["programming","ReactJS","javascript","jsx"],"created":"2025-01-05T00:45:23.787+08:00"}
---

---

```js
      {numPizzas > 0 ? (
        <ul className="pizzas">
          {pizzas.map((pizza) => (
            <Pizza pizzaObj={pizza} key={pizza.name} />
          ))}
        </ul>
      ) : <p>We're still working on our menu. Please come back later:)</p>}
```

>[!tip] Why not use `if-else` statement?
>You might ask, remember that in _JSX_ [[004  Rules of JSX  \| Statements are not allowed!]]