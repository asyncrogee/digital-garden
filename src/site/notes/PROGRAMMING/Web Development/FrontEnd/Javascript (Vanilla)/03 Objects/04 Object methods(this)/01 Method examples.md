---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/03-objects/04-object-methods-this/01-method-examples/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


# Method

---

A **function** that is a _property_ of an `object` is called its **_method_**.

```javascript
let user = {
  name: "John",
  age: 30,
};

user.sayHi = function () {
  alert("Hello!");
};

user.sayHi(); // Hello!
```

Here we used a Function Expression to create a function and assign it to the property `user.sayHi` of the **object**
then we call it as `user.sayHi()`. The user can now speak!

Pre-declared function as method:

```javascript
let user = {
  // ...
};

// first, declare
function sayHi() {
  alert("Hello!");
}

// then add as a method
user.sayHi = sayHi;

user.sayHi(); // Hello!
```

> [!tip] Method shorthand
> shorter syntax for methods in an object literal:
>
> ```javascript
> // these objects do the same
>
> user = {
>   sayHi: function () {
>     alert("Hello");
>   },
> };
>
> // method shorthand looks better, right?
> user = {
>   sayHi() {
>     // same as "sayHi: function(){ ... }"
>     alert("Hello");
>   },
> };
> ```
>
> - we can omit `"function"` and just write `sayHi()`.
