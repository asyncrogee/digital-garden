---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/01-basics/03-data-types/02-big-int/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:25:00.210+08:00"}
---


# 02 BigInt

---

Number type cannot represent integer values larger than (2^53 - 1) or **_9007199254740991_** or less than -(2^53 - 1) for negatives

a **_BigInt_** value is created by appending **n** to the end of an integer:

```javascript
// the "n" at the end means it's a BigInt
const bigInt = 1234567890123456789012345678901234567890n;
```
