---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/07-comparisons/01-comparisons-and-string-comparison/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


# 01 Comparisons & String Comparison

---

- **_Greater/less than_**: `a > b`, `a < b`
- **_Greater/less than or equals_**: `a >= b`, `a <= b`
- **_Equals_**:`a == b` - **Double Equal Signs**
  - Single equal sign means assignment: `a = b`
- **_Not equals_**: `a != b`

## String Comparison

To see if a string is greater than the other
JavaScript uses "dictionary" or "lexicographical" order.

```javascript
alert("Z" > "A"); // true
alert("Glow" > "Glee"); // true
alert("Bee" > "Be"); // true
```

> [!abstract]- Algorithm in comparing two strings
>
> - Compares the first character whether which are greater - If both strings are the same, it will compare the next letters/string until the one wins
>   > [!example] Glow and Glee
>   >
>   > 1. `G` is the same as `G`
>   > 2. `l` is the same as `l`
>   > 3. `o` is greater than `e`. Stop here. The first string is greater.

> [!Tip] Upper and lowercase letters are not equals
> `"A"` is not equal to the lowercase `"a"`
>
> - lowercase `"a"` is greater
