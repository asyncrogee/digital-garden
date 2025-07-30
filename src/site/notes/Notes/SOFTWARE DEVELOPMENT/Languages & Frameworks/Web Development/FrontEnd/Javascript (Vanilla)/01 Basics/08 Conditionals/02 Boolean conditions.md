---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/01-basics/08-conditionals/02-boolean-conditions/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:24:55.968+08:00"}
---

# 02 Boolean conditions

--- 
[[03 Boolean Conversion \| [ Boolean Conversion ] ]]

- number `0`, empty string `""`, `null`, `undefined`, and `NaN` are all `false`
	- They are called "__Falsy__" values.
- Other values become `true`, so they are called "__Truthy__"

```javascript
if (0) { // 0 is falsy
	...
}
```

```javascript
if (1) { // 1 is truthy
	...
}
```

We can also pass a pre-evaluated boolean value to `if`, like this:
```javascript
let cond = (year == 2015); // equality evaluates to true or false

if (cond) {
	...
}
```



