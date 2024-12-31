---
ProgrammingLanguage: JavaScript
tags:
  - programming
  - webdevelopment
  - frontend
  - JavaScript
dg-publish: true
---

# 02 BigInt

---

Number type cannot represent integer values larger than (2^53 - 1) or **_9007199254740991_** or less than -(2^53 - 1) for negatives

a **_BigInt_** value is created by appending **n** to the end of an integer:

```javascript
// the "n" at the end means it's a BigInt
const bigInt = 1234567890123456789012345678901234567890n;
```
