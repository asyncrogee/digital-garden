---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/002-components/004-sample-component-logic/","tags":["programming","ReactJS","javascript","components"]}
---

```js
function Footer() {
  const hour = new Date().getHours();
  const openHour = 12;
  const closeHour = 22;
  const isOpen = hour >= openHour && hour <= closeHour;
  console.log(isOpen);

  //   if (hour >= openHour && hour <= closeHour) alert("We're currently open!");
  //   else alert("Sorry we're closed");

  return (
    <footer>{new Date().toLocaleTimeString()}. We're currently open!</footer>
  );

  //   return React.createElement("footer", null, "We're currently open!");
}
```