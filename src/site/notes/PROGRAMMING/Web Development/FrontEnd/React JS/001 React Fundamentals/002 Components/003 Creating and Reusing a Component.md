---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/002-components/003-creating-and-reusing-a-component/","tags":["programming","ReactJS","javascript","components"]}
---


### Creating
`function Components()`, __must start with an Uppercase__

#### Using `JSX`:
```js
function Pizza() {
  return <h2>Pizza</h2>;
}
```

```js
function Pizza() {
  return (
    <div>
      <img src="pizzas/spinaci.jpg" alt="Pizza Spinaci" />
      <h2>Pizza Spinaci</h2>
      <p>Tomato, mozarella, mushrooms, and onion</p>
    </div>
  );
}
```
#### React Only:
```js
function Footer() {
  return React.createElement("footer", null, "We're currently open!");
}
```

---
### Nesting components:
```js
function App() {
  return (
    <div>
      <h1>Hello React!</h1>
      <Pizza />
    </div>
  );
}
```
- We _nest_ or used the `<Pizza />` inside `App()`
- Don't put the actual ___function declaration___ inside to nest, just do `<Comp />` like this.

> [!caution] 
> __Components can only return__ `1 element`
> So, to have multiple elements; We wrap them in a `<div>`
> ```js
> Function App() {
> 	return (
> 		<div>
> 			<h1>Hello React!</h1>
> 			<Pizza />
> 		</div>
> 	);
> }
> ```


