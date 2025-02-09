---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/00-essential-java-script/10-array-reduce-method/","tags":["programming","jsbasics","javascript","JS-Fundamentals"],"created":"2024-12-24T20:45:47.309+08:00"}
---


> [!abstract] reduce method
> Reduces/Boil down the entire array into _1 value_
> - _first value_: Callback function 
> - _second value_: Starter value


```js
const pagesAllBooks = books.reduce((accumulator, book) => accumulator + book.pages, 0)
```
- `0` is the starting value of the ___`accumulator`___
	- then in the callback function, it's getting added. 
- Conceptually, I think it looks like the __iterations in a `for loop`__

