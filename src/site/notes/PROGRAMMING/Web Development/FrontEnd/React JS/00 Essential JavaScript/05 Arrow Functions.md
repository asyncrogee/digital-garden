---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/00-essential-java-script/05-arrow-functions/","tags":["programming","jsbasics","javascript","JS-Fundamentals"]}
---



>[!info] 
>Common way of writing a function
>or a [[01 Function declaration \| Function Declaration]]
>```javascript
>function getYear(str) {
>	return str.split("-")[0];
>}
>```


> [!example] Arrow Function
> [[07 Function expressions \| Function Expression]]
> ```javascript
> // Example: publicationDate = 1954-10-21
> const getYear = (str) => str.split("-")[0];
> ```
> 
> ```javascript
> const summary = `${title}, a ${pages}-page long book, was written by ${author} and published in ${getYear(publicationDate)}. The book has ${hasMovieAdaptation ? "" : "not"} been adapted as a movie`;
> ```



[[00 PROGRAMMING/Web Development/FrontEnd/Javascript (Vanilla)/01 Basics/12 Functions/07 Function expressions.md\|00 PROGRAMMING/Web Development/FrontEnd/Javascript (Vanilla)/01 Basics/12 Functions/07 Function expressions.md]]

