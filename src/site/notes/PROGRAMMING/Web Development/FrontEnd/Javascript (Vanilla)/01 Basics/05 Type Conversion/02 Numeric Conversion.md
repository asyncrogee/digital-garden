---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/05-type-conversion/02-numeric-conversion/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


# 02 Numeric Conversion

---

Numeric conversion in mathematical functions and expressions happens automatically.

Example, when division **_/_** is applied to **non-numbers**:

```javascript
alert("6" / "2"); // 3, strings are converted to numbers
```

To convert a **_value_** to a number:
`Number(value)`

```javascript
let str = "123";
alert(typeof str); // strings

let num = Number(str); // becomes a number 123
alert(typeof num); // number
```

If the **string is not a valid number**,
the result of such a conversion is **_NaN_**:

```javascript
let age = Number("an arbitrary string instead of a number");

alert(age);
```

> [!EXAMPLE] Numeric conversion rules:
>
> | Value          | Becomes...                                                                                                                                                                                                                          |
> | -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
> | null           | 0                                                                                                                                                                                                                                   |
> | true and false | 1 and 0                                                                                                                                                                                                                             |
> | string         | Whitespaces (includes spaces, tabs \\t, new lines \\n etc.) from the start and end are removed. If the remaining string is empty, the result is **_0_**. Otherwise, the number is "read" from the string. An error gives **_NaN_**. |
>
> ```javascript
> alert(Number("   123   ")); // 123
> alert(Number("123z")); // NaN (error reading a number at "z")
> alert(Number(true)); // 1
> alert(Number(false)); // 0
> ```

> [!Note] **null** and _undefined_ behave differently here:
>
> - **null** becomes zero
> - _undefined_ becomes **_NaN_**
