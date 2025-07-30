---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/01-basics/03-data-types/01-number/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:25:00.213+08:00"}
---


# 01 Number

---

Represents both **integer** and **floating point** numbers.

Besides regular numbers,
there are so-called "**_special numeric values_**":
`Infinity`, `-Infinity` and `NaN`.

- `Infinity`
  - division by zero:

```javascript
alert(1 / 0); // Infinity
```

- or reference it directly:

```javascript
alert(Infinity); // Infinity
```

- `NaN`
  - Computational error
  - Incorrect or undefined math operation

```javascript
alert("not a number" / 2); // NaN, such division is erroneous
```

- If there's **NaN** in math expression, it will also be the result.
  - EXCEPT: **NaN \*\* 0** is **_1_**.
