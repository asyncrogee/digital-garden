---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/dom/03-handling-click-events/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:24:56.654+08:00"}
---


---

# Handling Click events

---

> [!info]
>
> ```javascript
> document.querySelector.('.check').addEventListener('click')
>
> document.querySelector.('.check').addEventListener('click', function() {
> 	console.log(document.querySelector('.guess').value);
>
> 	document.querySelector('.message').textContent = 'Correct Number!';
> });
> ```
>
> - First argument `('click', ... );`, is the **name of the event** we're listening for.
> - Second argument `( ..., function() {});`, is the **function that will execute** once the event happens.

> [!example]
>
> ```javascript
> document.querySelector(".check").addEventListener("click", function () {
>   const guess = Number(document.querySelector(".guess").value);
>   console.log(guess, typeof guess);
>
>   if (!guess) {
>     document.querySelector(".message").textContent = "No number!";
>   }
> });
> ```
