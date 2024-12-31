---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/12-functions/07-function-expressions/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---

# 01 Function expressions

--- 
No matter how the function is created, a function is a __value__.
>[!info]- Function is a value representing an "action"
>- Regular values like strings or numbers represent the ___data___
>- A function can be perceived as an ___action___
>- We can pass it between variables and run when we want

>[!caution]- Declaration vs Expression difference?
> - Function Declaration can be called, _before_ defining the function.
> ```javascript
> const age1 = calcAge1(1991);
> 
> function calcAge1(birthYear) {
> 	return 2037 - birthYeah;
> }
> ```
>  - Function Expression can't, it will result to an ___Error___
>```javascript
>// this will result to an ERROR:
>console.log(age1, age2);
>
>const calcAge2 = function(birthYear) {
>	return 2037 - birthYear;
>}
>
>// console.log(age1, age2);
>```


>[!tip] Function Expression
> Function is a special kind of value
>```javascript
>let sayHi = function() {
>	alert( "Hello" );
>};
>```

>[!abstract] Function in JavaScript
>not like the functions in other programming language, where mentioning the function name causes its execution.
>JavaScript treats function a value
>```javascript
>function sayHi() {
>	alert( "Hello" );
>}
>
>alert( sayHi ); //shows the function code
>```

>[!tip] Copy a function to another variable
>```javascript
>function sayHi() { // (1) create
>	alert( "Hello" );
>}
>
>let func = sayHi; // (2) copy
>
>func(); // Hello  //(3) run the copy (it works)!
>sayHi(); // Hello // this still works too (why wouldn't it)
>```
>- the Function Declaration `(1)` creates the function and put into the variable named `sayHi`
>- Line `(2)` copies it into the variable `func`
>	- Note: There's no parentheses `()` after `sayHi`, if there is `func = sayHi()`would store `sayHi()`_result_ into `func`. __NOT the function__ `sayHi` itself.
> - Now the function can be called as both `sayHi()` and `func()`
> ```javascript
> let sayHi = function() { // (1) create
> 	alert( "Hello" );
> };
> 
> let func = sayHi;
> // ...
> ```

>[!question] Why is there a `semicolon` at the end?
> ```javascript
> function sayHi() {
> 	// ...
> }
> 
> let sayHi = function() {
> 	// ...
> };
> ```
> >[!DONE] Answer
> > - a Function Expression is created as `function(...) {...}` inside the assignment statement: `let sayHi = ...;`.
> > - The semicolon `;` is recommended at the end, it's not a part of the function syntax
> > - It's there for a simpler assignment
> > 	- like `let sayHi = 5;`

---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/programming/web-development/front-end/javascript-vanilla/01-basics/12-functions/01-function-declaration/#function-inside-a-code-block" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Function Inside a Code Block

> [!INFO] Function Declaration
>
> ```javascript
> function sayHi() {
>   alert("Hello");
> }
> ```
>
> > [!danger] Function Declaration within a code block
> >
> > - If a Function Declaration is inside a **code block**,
> >   - It's visible only inside that block
> > - BUT, Not outside of it.
> >
> > ```javascript
> > let age = prompt("What is your age?", 18);
> >
> > // conditionally declare a function
> > if (age < 18) {
> >   function welcome() {
> >     alert("Hello!");
> >   }
> > } else {
> >   function welcome() {
> >     alert("Greetings!");
> >   }
> > }
> >
> > // ... use it later
> > welcome(); // Error:  welcome is not defined
> > ```
> >
> > > [!example] Another Example:
> > >
> > > ```javascript
> > > let age = 16; // take 16 as an example
> > >
> > > if (age < 18) {
> > >   // (runs)
> > >   welcome();
> > >
> > >   function welcome() {
> > >     // Function declaration is avai
> > >     alert("Hello!"); // everywhere in the block where it's declared
> > >   }
> > >
> > >   welcome();
> > >   // (runs)
> > > } else {
> > >   function welcome() {
> > >     alert("Greetings!");
> > >   }
> > > }
> > >
> > > // Here we're out of curly braces,
> > > // so we can not see Function Declarations made inside of them
> > >
> > > welcome(); // Error: welcome is not defined
> > > ```

---


</div></div>


>[!DONE] We are able to do this with Function Expression:
>```javascript
>let age = prompt("What is your age?", 18);
>
>let welcome;
>
>if (age < 18) {
>	welcome = function {
>		alert("Hello!");
>	};
>} else {
>	welcome = function() {
>		alert("Greetings!");
>	};
>}
>
>welcome(); // ok now
>```
>>[!tip] Simplify further using Ternary/Question mark operator `?`:
>>```javascript
>>let age = prompt("What is your age?", 18);
>>
>>let welcome = (age < 18)?
>>	function() { alert("Hello!"); } :
>>	function () { alert("Greetings!"); };
>>	
>>	welcome(); // ok now
>>```
