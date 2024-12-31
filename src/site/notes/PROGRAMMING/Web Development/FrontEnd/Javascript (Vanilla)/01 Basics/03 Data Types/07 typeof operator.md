---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/03-data-types/07-typeof-operator/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


# 07 typeof operator

---

Returns the type of the operand.

- typeof is an **operator**, not a function

**_typeof(x)_** is the same as **typeof x**

```javascript
typeof undefined; // "undefined"
typeof 0; // "number"
typeof true; // "boolean"
typeof "foo"; // "string"
typeof Symbol("id"); // "symbol"
```

```javascript
typeof Math; // "object"
```

- **_Math_** is a built-in object that provides mathematical operations.

```javascript
typeof null; // "object"
```

- **_null_** is NOT an object
- It's a special value
- **typeof**'s behavior is wrong

```javascript
typeof alert; // "function"
```

- alert is a function
- Functions belong to the object type
