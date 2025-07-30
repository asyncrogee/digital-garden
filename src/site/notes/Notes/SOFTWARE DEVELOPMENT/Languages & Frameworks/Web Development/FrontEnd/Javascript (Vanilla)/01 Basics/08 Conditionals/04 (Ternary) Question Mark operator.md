---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/01-basics/08-conditionals/04-ternary-question-mark-operator/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:24:55.960+08:00"}
---


# 04 Question Mark operator

---

"conditional" or "question mark" operator `?`

> [!Tip] Syntax:
>
> ```javascript
> condition ? exprIfTrue : exprIfFalse;
>
> let result = condition ? value1 : value2;
> ```

> [!info]
>
> - Represented by a question mark `?`
> - Sometimes called "**ternary**"
>   - because it has **_Three operands_**
>   - One and only operator in JavaScript which has that many

It let us do this in shorter way:

```javascript
let accessAllowed;
let age = prompt("How old are you?", "");

if (age > 18) {
  accessAllowed = true;
} else {
  accessAllowed = false;
}

alert(accessAllowed);
```

```javascript
let accessAllowed = age > 18 ? true : false;
//OR

// the comparison operator "age > 18" executes first anyway
// (no need to wrap it into parentheses)
let accessAllowed = age > 18 ? true : false;
```

> [!note]
> The comparison itself returns `true/false` - There's no need to use the **question mark / ternary operator** just like the code above.
>
> ```javascript
> // the same
> let accessAllowed = age > 18;
> ```

---

> [!Caution] Not recommended way of using Ternary operator:
> It may be shorter but not readable compared to using `if...else`
>
> ```javascript
> let company = prompt("Which company created JavaScript?", " ");
>
> company == "Netscape" ? alert("Right!") : alert("Wrong.");
> ```
>
> We didn't assigned result to a variable here, instead it executed different code depends on the condition.
>
> `If...else` version:
>
> ```javascript
> let company = prompt("Which company created JavaScript?", " ");
>
> if (company == "Netscape") {
>   alert("Right!");
> } else {
>   alert("Wrong.");
> }
> ```

---

## More Example:
