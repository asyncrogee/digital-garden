---
{"dg-publish":true,"permalink":"/00-programming/web-development/front-end/react-js/00-essential-java-script/01-destructuring-objects-and-arrays/","tags":["programming","jsbasics","javascript","JS-Fundamentals"]}
---

# Destructuring Objects and Arrays

--- 

> [!tip] Object Destructuring
> ```javascript
> const book = getBook(2);
> 
> const title = book.title;
> const author = book.author;
> ```
> We can __shorten__ these codes by ___destructuring objects___:
> ```javascript
> const {title, author} = book;
> ```
> - inside `{ }` the __variable names__ should be the __same as the__ ___property names___

> [!tip] Destructuring Arrays
> Same thing with Destructuring Objects
> ```javascript
> const primaryGenre = genres[0];
> const secondaryGenre = genres[1];
> 
> // the same as above:
> const [primaryGenre, secondaryGenre] = genres;
> ```
