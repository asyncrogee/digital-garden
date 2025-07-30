---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/01-basics/06-basic-operators/07-modify-in-place/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:24:55.897+08:00"}
---


# 07 Modify-in-place

---

```javascript
let n = 2;

n = n + 5;
n += 5; // n = 7 (same as n = n + 5)

n = n * 2;
n *= 2; // n = 14 (same as n = n * 2)

alert(n); // 14
```

```javascript
let n = 2;

n *= 3 + 5; // right part evaluated first, same as n *= 8

alert(n); // 16
```
