---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/03-objects/08-object-to-primitive-conversion/03-to-string-and-value-of/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:24:56.574+08:00"}
---


---

# toString/valueOf

---

If there's no `Symbol.toPrimitive`,
JavaScript tries to find methods `toString` and `valueOf`:

- Call `toString` method for **string hint**
  - If it _doesn't exist_ or if it returns an _object instead of a primitive value_, then call `valueOf`
- **For other hints**, call `valueOf`
  - if it _doesn't exist_ or if it returns an _object instead of a primitive value_, then call `toString`

> [!example] by Default
> a **plain object** has following `toString` and `valueOf` methods:
>
> - `toString` method returns a string `"[object Object]"`.
> - `valueOf` method returns the **object itself**.
>
> ```javascript
> let user = { name: "John" };
>
> alert(user); // [object Object]
> alert(user.valueOf() === user); // true
> ```

> [!tip] Combination of `toString` and `valueOf` > `user` does the same as above using a **combination** of `toString` and `valueOf` instead of [[02 Symbol to Primitive \| Symbol.toPrimitive]]:
>
> ```javascript
> let user = {
>   name: "John",
>   money: 1000,
>
>   // for hint="string"
>   toString() {
>     return `{name: "${this.name}"}`;
>   },
>
>   // for hint="number" or "default"
>   valueOf() {
>     return this.money;
>   },
> };
>
> alert(user); // toString -> {name: "John"}
> alert(+user); // valueOf -> 1000
> alert(user + 500); // valueOf -> 1500
> ```
>
> It does the same thing as `Symbol.toPrimitive`.

> [!tip] `toString` only
> Single "catch-all" place to handle all primitive conversions.
>
> ```javascript
> let user = {
>   name: "John",
>
>   toString() {
>     return this.name;
>   },
> };
>
> alert(user); // toString -> John
> alert(user + 500); // toString -> John500
> ```

> [!caution] A conversion can return **any primitive type**
> Primitive-conversion methods do not necessarily **return the "hinted" primitive**
>
> There is no control whether `toString` returns **_exactly a string_**,
> or whether `Symbol.toPrimitive` method returns a number for the hint `number`.
>
> The only mandatory thing: **these methods must return a primitive, not an object**.
