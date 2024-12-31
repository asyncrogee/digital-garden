---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/07-comparisons/04-strict-equality/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


# 04 Strict equality

---

> [!danger]- Problem
> A regular equality check `==` cannot differentiate `0` from `false`.
>
> ```javascript
> alert(0 == false); // true
> ```
>
> same thing with empty string:
>
> ```javascript
> alert("" == false); // true
> ```
>
> > [!question]- Why?
> > Operands of different types are converted to numbers by the equality operator `==`
> > Empty string like `false`, becomes a zero.

To differentiate `0` from `false`
Use **_String Equality Operator_** `===`

- Checks the equality without type conversion.
- If `a` and `b` are of different types
  - `a === b` immediately returns `false`
    - without an attempt to converting them

```javascript
alert(0 === false); // false, because the types are different
```

There's also **Strict Non-equality** operator `!==`
