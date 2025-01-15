---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/05-type-conversion/03-boolean-conversion/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:41.838+08:00"}
---


# 03 Boolean Conversion

---

[[04 Boolean \| [ Boolean ]]]

## Truthy and Falsy

> [!Example] Conversion Rule:
>
> - Values that are intuitively "empty", like:
>   - **_0_**
>   - an empty string
>   - **_null_**
>   - **_undefined_**
>   - **_NaN_**
> - become **False**
> - Other values become **True**
>
> | Value                                 | Becomes… |
> | ------------------------------------- | -------- |
> | `0`, `null`, `undefined`, `NaN`, `""` | `false`  |
> | any other value                       | `true`   |

```javascript
alert(Boolean(1)); // true
alert(Boolean(0)); // false

alert(Boolean("hello")); // true
alert(Boolean("")); // false
```

String with zero **_"0"_** is **true**

```javascript
alert(Boolean("0")); // true
alert(Boolean(" ")); // spaces, also true (any non-empty string is true)
```
