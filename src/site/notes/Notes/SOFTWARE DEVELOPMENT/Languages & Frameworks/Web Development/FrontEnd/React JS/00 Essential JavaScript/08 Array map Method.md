---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/00-essential-java-script/08-array-map-method/","tags":["programming","jsbasics","javascript","JS-Fundamentals"],"created":"2025-07-13T15:24:50.885+08:00"}
---


> [!abstract] Array Map method
> - __Loops__ over an `array`
> - Returns a new `array` with the _same length_
> - with __some operation applied__

```javascript
const x = [1, 2, 3, 4, 5].map((el) => el * 2);
console.log(x); // [ 2, 4, 6, 8, 10 ]
```

```js
const title = books.map((book) => book.title);
```
- returns an `array` of all the titles of the `books`


#### Not using an `arrow function`:
###### with `return`
```js
const title = books.map((book) => {
	return {
		title: book.title,
		author: book.author,
	};
});
```

###### No `return`
```js
const title = books.map((book) => ({
	title: book.title,
	author: book.author,
	reviewsCount: getTotalReviewCount(book),
}))
```

