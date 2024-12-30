---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/00-essential-java-script/11-array-sort-method/","tags":["programming","jsbasics","javascript","JS-Fundamentals"]}
---


#### Sorting in Ascending & Descending order:

```js
const arr = [3, 7, 1, 9, 6];

// ASCENDING:
const sorted = arr.sort((a, b) => a - b); // output: [1, 3, 6, 7, 9]

// DESCENDING:
const sorted = arr.sort((a, b) => b - a); // output: [9, 7, 6, 3, 1]
```

###### Warning:
> This modifies the original array:
```js
const arr = [3, 7, 1, 9, 6]; // becomes: [1, 3, 6, 7, 9]
const sorted = arr.sort((a, b) => a - b); // output: [1, 3, 6, 7, 9]
```
- If the `a - b` or the callback function returns a _negative_, it will be __sorted in ascending way (small first)__

> Adding `.slice()` creates a copy of that array to ___preserve the original data___
```js
const arr = [3, 7, 1, 9, 6]; // still the same: [1, 3, 6, 7, 9]
const sorted = arr.slice().sort((a, b) => a - b); // output: [1, 3, 6, 7, 9]
```

> [!example] Book Pages Sorting
> ```js
> const sortedByPages = books.slice().sort((a, b) => a.pages - b.pages);
> ```
