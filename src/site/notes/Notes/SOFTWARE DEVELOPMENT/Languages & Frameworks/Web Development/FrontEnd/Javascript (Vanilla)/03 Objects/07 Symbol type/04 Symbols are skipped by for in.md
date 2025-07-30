---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/03-objects/07-symbol-type/04-symbols-are-skipped-by-for-in/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:24:56.605+08:00"}
---

# Symbols are skipped by for...in

--- 
Symbolic properties __do not participate__ in `for...in` loop.

```javascript
let id = Symbol("id");
let user = {
	name: "John",
	age: 30,
	[id]: 123
};

for (let key in user) alert(key); // name, age (no symbols)

// the direct access by the symbol works
alert( "Direct: " + user[id] ); // Direct: 123
```



If another script or library __loops over our object__, it won't unexpectedly access a `symbolic property`


### Object.keys(user)
 `Object.keys(user)` also ignores them.

### Object.assign

`Obbject.assign` copies __both__ `string` and `symbol` properties:
```javascript
let id = Symbol("id");
let user = {
	[id]: 123
};

let clone = Object.assign({}, user);

alert( clone[id] ); // 123
```