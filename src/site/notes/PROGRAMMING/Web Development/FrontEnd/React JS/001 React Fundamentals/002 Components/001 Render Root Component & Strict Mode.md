---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/002-components/001-render-root-component-and-strict-mode/","tags":["programming","ReactJS","javascript","components"],"created":"2024-12-28T13:59:31.141+08:00"}
---

## Rendering Root in React 18
```js
import React from "react";
import ReactDOM from "react-dom/client";
```
- This is where we import __React__ from the ___node_modules___
	- There's another way using `script` tag, but in React application we don't do that:
	- ![Pasted image 20241228140405.png](/img/user/Misc/attachments/Pasted%20image%2020241228140405.png)

```js
function App() {
  return <h1>Hello React!</h1>;
}
```
- The function name doesn't need to be named `App`, it's just a common name convention
- A _'status' component_ (like `App()`) have to __start with an UPPERCASE__

```js
const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<App />);
```
- here, we render the `App` component into the `root` id element from _index.html_ in "public" folder using ___ReactDOM___'s `createRoot` function

## Strict Mode
Renders _components_ ___twice___ to __find certain bugs__
```js
...
root.render(
	<React.StrictMode>
		<App />
	</React.StrictMode>
);
```
