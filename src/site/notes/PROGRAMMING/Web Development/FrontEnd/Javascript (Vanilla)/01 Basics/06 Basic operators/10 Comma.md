---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/06-basic-operators/10-comma/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


# 10 Comma

---

Used to write shorter code

Allows to evaluate several expressions

- Dividing them with a comma `,`
- Each of them is evaluated but only the result of the last one is returned.

```javascript
let a = (1 + 2, 3 + 4);

alert(a); // 7 (the result of 3 + 4)
```

The first expression `1 + 2` is evaluated and its **result is thrown away**.

Then, `3 + 4` is evaluated and **_returned as the result_**.

> [!Caution] Comma has a very low precedence
> Lower than `=`, **parentheses** are important
> Without parentheses `a = 1 + 2, 3 + 4`
>
> - Summing the numbers into `a = 3, 7`
> - then `=` assigns `a = 3`
> - the **rest is IGNORED**

Example:

```javascript
// three operations in one line
for (a = 1, b = 3, c = a * b; a < 10; a++){
...
}
```
