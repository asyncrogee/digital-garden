---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/00-essential-java-script/09-array-filter-method/","tags":["programming","jsbasics","javascript","JS-Fundamentals"],"created":"2025-07-13T15:24:50.881+08:00"}
---


Adds a value in an `array` ONLY if the ___condition___ returns __true__
```js
const longBooks = books.filter((book) => book.pages > 500);
```
- Adds each `book` that has more than ___500 pages___

#### Chaining `.filter()`
```js
const longBooksWithMovie = books.filter((book) => book.pages > 500).filter((book) => book.hasMovieAdaptation);

// with proper format:
const longBooksWithMovie = books
	.filter((book) => book.pages > 500)
	.filter((book) => book.hasMovieAdaptation);
```

##### Combination of `.filter()` and `.map()`
```js
const adventureBooks = books.filter((books) => books.genres.includes("adventure")).map((book) => book.title);
```
- Filters `books` that has the genre `adventure`
	- and only store the `book.title` in `adventureBooks` array variable.