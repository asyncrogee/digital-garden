---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/01-basics/08-conditionals/03-else-and-else-if-clause/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:24:55.964+08:00"}
---


# 03 Else & else if clause

---

The `else` block executes when `if` statement is false.

```javascript
let year = prompt(
  "In which year was the ECMAScript-2015 specification published?",
  ""
);

if (year == 2015) {
  alert("You guessed it right!");
} else {
  alert("How can you be so wrong?"); // any value except 2015
}
```

## Else if

Let us test several variants of a condition with `else if`

```javascript
let year = prompt(
  "In which year was the ECMAScript-2015 specification published?",
  ""
);

if (year < 2015) {
  alert("Too early...");
} else if (year > 2015) {
  alert("Too late");
} else {
  alert("Exactly!");
}
```

- JavaScript checks `year < 2015`,
  - if false, goes to the next condition `year > 2015`
    - If false again, it shows the `else`'s `alert`
