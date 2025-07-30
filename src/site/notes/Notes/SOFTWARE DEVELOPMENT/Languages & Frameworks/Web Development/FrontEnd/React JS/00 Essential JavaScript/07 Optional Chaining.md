---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/00-essential-java-script/07-optional-chaining/","tags":["programming","jsbasics","javascript","JS-Fundamentals"],"created":"2025-07-13T15:24:50.889+08:00"}
---


```js
function getTotalReviewCount(book) {
	const goodreads = book.reviews.goodreads.reviewsCount;
	const librarything = book.reviews.librarything.reviewsCount;
	return goodreads + librarything;
}

console.log(getTotalReviewCount(book)); // 812
```

but, what if the `book` doesn't have a review in `librarything` ?
It will result into an ___`Cannot read properties of undefined (reading 'reviewsCount')`___ error.

---

### Optional Chaining
[[Notes/SOFTWARE DEVELOPMENT/Languages & Frameworks/Web Development/FrontEnd/Javascript (Vanilla)/03 Objects/06 Optional chaining/01 non-existing property Problem\| Optional Chaining (Non-existing Property Problem)]]

```js
function getTotalReviewCount(book) {
	const goodreads = book.reviews.goodreads.reviewsCount;
	const librarything = book.reviews.librarything?.reviewsCount ?? 0;
	return goodreads + librarything;
}

console.log(getTotalReviewCount(book)); // 812
```
- `book.reviews.librarything?.reviewsCount` 
	- tells JavaScript to continue reading ___properties___ __only if what comes before it exists__
		- in this case, if `book.reviews.librarything` exists, it will continue reading the next property:`reviewsCount`