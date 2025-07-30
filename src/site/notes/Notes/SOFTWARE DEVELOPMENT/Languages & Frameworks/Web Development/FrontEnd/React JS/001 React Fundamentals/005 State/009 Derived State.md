---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/001-react-fundamentals/005-state/009-derived-state/","tags":["programming","ReactJS","javascript","state","derivedstate"],"created":"2025-07-13T15:25:33.874+08:00"}
---


> [!abstract] Derived State
> `state` that is computed from an __existing__ piece of `state` or from `props`

> [!caution] Common beginner mistake:
> Three separate pieces of `state`, even though `numItems` and `totalPrice` depends on the cart:
> ```jsx
> const [cart, setCard] = useState([
> 	{ name: "JavaScript Course", price: 15.99 },
> 	{ name: "Node.js Bootcamp", price: 14.99 },
> ]);
> const [numItems, setNumItems] = useState(2);
> const [totalPrice, setTotalPrice] = useState(30.98);
> ```
> - 👎 Need to keep them in sync (update together)
> - 👎 3 `state` updates will cause 3 re-renders

> [!done] Deriving state
> ```jsx
> const [cart, setCard] = useState([
>	{ name: "JavaScript Course", price: 15.99 },
>	{ name: "Node.js Bootcamp", price: 14.99 },
>]);
>
>const numItems = cart.length;
>const totalPrice = cart.reduce((acc, cur) => acc + cur.price, 0);
> ```
> - 👍 Just regular variables, no `useState`
> - 👍 `cart` state is the __single source of truth__ for this related data
> - 👍 Works because re-rendering `component` will __automatically re-calculate__ derived `state`

