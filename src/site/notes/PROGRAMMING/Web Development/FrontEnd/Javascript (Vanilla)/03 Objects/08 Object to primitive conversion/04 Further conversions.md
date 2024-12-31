---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/03-objects/08-object-to-primitive-conversion/04-further-conversions/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


---

# Design

---

> [!info]
> Many `operators` and `functions` perform type conversions
> Example:
> Multiplication `*` **converts operands to numbers**
>
> If we pass an `object` as an **_argument_**,
> there are two stages of calculations:
>
> 1. `Object` is **converted to primitive**
> 2. If necessary, the **resulting primitive** is also **_converted_**.
>
> ```javascript
> let obj = {
>   // toString handles all conversions in the absence of other methods
>   toString() {
>     return "2";
>   },
> };
>
> alert(obj * 2); // 4, object converted to primitive "2", then multiplication made it a number
> ```
>
> 1. The _multiplication_ `obj * 2` first **converts the object to primitive** (string `"2"`)
> 2. Then `"2" * 2` becomes `2 * 2` (the string is converted to number).

Binary plus will **concatenate strings** in the same situation

```javascript
let obj = {
  toString() {
    return "2";
  },
};

alert(obj + 2); // 22 ("2" + 2), conversion to primitive returned a string => concatenation
```
