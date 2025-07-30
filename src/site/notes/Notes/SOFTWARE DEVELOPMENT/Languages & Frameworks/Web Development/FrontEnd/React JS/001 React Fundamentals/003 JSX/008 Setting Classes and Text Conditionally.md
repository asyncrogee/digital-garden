---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/001-react-fundamentals/003-jsx/008-setting-classes-and-text-conditionally/","tags":["programming","ReactJS","javascript"],"created":"2025-07-13T15:25:33.847+08:00"}
---

#### Conditional Classes:
```js
function Pizza({ pizzaObj }) {
  // if (pizzaObj.soldOut) return null;
  
  return (
    <li className={`pizza ${pizzaObj.soldOut ? "sold-out" : ""}`}>
      <img src={pizzaObj.photoName} alt={pizzaObj.name} />
```

#### Conditional Text:
Two variants:
- Straight Text:
```js
<span>{pizzaObj.soldOut ? "SOLD OUT" : pizzaObj.price}</span>
```

- with `<span>`:
```js
<span>
  {pizzaObj.soldOut ? (
	<span>SOLD OUT</span>
  ) : (
	<span>{pizzaObj.price}</span>
  )}
</span>
```


