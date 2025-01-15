---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/04-data-types/01-numbers/02-hex-binary-and-octal-numbers/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:33.262+08:00"}
---

---
# Hex, Binary and Octal

--- 

> [!info] Hexadecimal
> widely use in JavaScript to __represent colors__, __encode characters__, and for many other things.
> shorter way to write them: `0x` and then ___the number___.
> ```javascript
> alert( 0xff ); // 255
> alert( 0xFF ); // 255 (the same, case doesn't matter)
> ```

>[!info] Binary & Octal
>```javascript
>let a = 0b11111111; // binary form of 255
>let b = 0o377; // octal form of 255
>
>alert ( a == b ); // true, the same number 255 at both sides
>```
