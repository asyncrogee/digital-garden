---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/03-objects/08-object-to-primitive-conversion/02-symbol-to-primitive/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:33.382+08:00"}
---


---

# Symbol.toPrimitive

---

`Symbol.toPrimitive` is a built-in symbol.
Should be used to **name the conversion method**

```javascript
obj[Symbol.toPrimitive] = function (hint) {
  // here goes the code to convert this object to a primitive
  // it must return a primitive value
  // hint = one of "string", "number", "default"
};
```

if method `Symbol.toPrimitive` exists, **it's used for ALL HINTS**, and no more methods are needed.

For instance, `user` object implements it:

```javascript
let user = {
  name: "John",
  money: 1000,

  [Symbol.toPrimitive](hint) {
    alert(`hint: ${hint}`);
    return hint == "string" ? `{name: "${this.name}"}` : this.money;
  },
};

// conversions demo:
alert(user); // hint: string -> {name: "John"}
alert(+user); // hint: number -> 1000
alert(user + 500); // hint: default -> 1500
```
