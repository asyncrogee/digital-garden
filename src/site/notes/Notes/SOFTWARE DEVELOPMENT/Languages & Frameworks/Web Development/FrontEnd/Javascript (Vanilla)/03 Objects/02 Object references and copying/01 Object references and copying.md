---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/03-objects/02-object-references-and-copying/01-object-references-and-copying/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:24:56.459+08:00"}
---


# Object references and copying

---

When an object variable is copied, the _reference_ is copied, but the **object itself is not duplicated**.

> [!info]- Why?
> _Primitive_ values: `string`, `numbers`, `booleans`, etc. are always copied "**as a whole value**".
>
> ```javascript
> let message = "Hello!";
> let phrase = message;
> ```
>
> `message` and `phrase` are independent variables storing the same value `Hello!`.
>
> **Objects** are stored and copied "**by reference**".
> A `variable` in an `object` stores the "address in memory" of the `object`.
>
> ```javascript
> let user = {
>   name: "John",
> };
> ```
>
> ![[Pasted image 20240113224905.png \|300]]
> The `object` is stored somewhere in memory (at the right of the picture), while `user` variable has a "**reference**" to it.

```javascript
let user = { name: "John" };

let admin = user; // copy the reference
```

![[Pasted image 20240114112903.png \| 500]]
There's still **one object**, but `two variables` that _reference it._

> [!tip] Use either variable to access and modify the object:
>
> ```javascript
> let user = { name: "John" };
>
> let admin = user;
>
> admin.name = "Pete"; // changed by the "admin" reference
>
> alert(user.name); // 'Pete', changes are seen from the 'user' reference
> ```

## Comparison by reference

`Two objects` are _equal only_ if they are the `same object`.

```javascript
let a = {};
let b = a; // copy the reference
alert(a == b); // true, both variables reference the same object
alert(a === b); // true
```

These `two independent objects` are **not equal**, even tho they're both _empty_.

```javascript
let a = {};
let b = {}; // two independent objects

alert(a == b); // false
```

> [!important] `const` objects can be **modified**
>
> ```javascript
> const user = {
>   name: "John",
> };
>
> user.name = "Pete";
>
> alert(user.name); // Pete
> ```
>
> The _value_ of `user` is **constant**, it must always **reference the same object**, but `properties` of that object are _free to change._
>
> It will only give an error if we try to set `user=...` as a **WHOLE**.
