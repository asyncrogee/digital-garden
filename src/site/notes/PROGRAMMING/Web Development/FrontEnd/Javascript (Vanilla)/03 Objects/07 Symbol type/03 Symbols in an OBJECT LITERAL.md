---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/03-objects/07-symbol-type/03-symbols-in-an-object-literal/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:33.293+08:00"}
---


# Symbol in Object Literal

---

> [!info]- Object Literal
> a straightforward and concise way to define objects in JavaScript.
>
> ```javascript
> let person = {
>   name: "John",
>   age: 30,
>   city: "New York",
> };
> ```

**Square brackets** are needed when using a `Symbol` in an object literal.

```javascript
let id = Symbol("id");

let user = {
  name: "John",
  [id]: 123,
};
```

Because we need the **value** from variable `id` as the key,
NOT the string `"id"`.
