---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/00-essential-java-script/04-ternaries-instead-of-ifelse-statements/","tags":["programming","jsbasics","javascript","JS-Fundamentals"],"created":"2025-07-13T15:24:56.669+08:00"}
---

>[!example]
>```javascript
>const pagesRange = pages > 1000 ? "over a thousand" : "less than 1000"; // over a thousand
>```
>
>```javascript
>const summary = `${title}, a ${pages}-page long book, was written by ${author} and published in ${publicationDate.split("-")[0]}. The book ${hasMovieAdaptation ? "" : "not"} been adapted as a movie`;
>```





<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/01-basics/08-conditionals/04-ternary-question-mark-operator/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">





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


</div></div>
