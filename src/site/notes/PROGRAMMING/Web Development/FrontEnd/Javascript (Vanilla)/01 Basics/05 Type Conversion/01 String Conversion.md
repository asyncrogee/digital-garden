---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/05-type-conversion/01-string-conversion/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:41.802+08:00"}
---


# 01 String Conversion

---

Happens when we need the string form of a value.

To convert value to a string:
`String(value)`

```javascript
let value = true;
alert(typeof value); // boolean

value = String(value); // now value is a string "true"
```

A `false` becomes **_"false"_**,
`null` becomes **_"null"_**, etc.
