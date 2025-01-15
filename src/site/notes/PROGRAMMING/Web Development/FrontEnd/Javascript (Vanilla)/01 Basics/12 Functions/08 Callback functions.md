---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/12-functions/08-callback-functions/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:42.522+08:00"}
---


# 02 Callback functions

---

```javascript
function ask(question, yes, no) {
  if (confirm(question)) yes();
  else no();
}

function showOk() {
  alert("You agreed.");
}

function showCancel() {
  alert("You canceled the execution");
}

// usage: functions showOK, showCancel are passed as arguments to ask
ask("Do you agree?", showOk, showCancel);
```

The function ask the `question` and, depends on the user's answer, call `yes()` or `no()`

- Arguments `showOk` and `showCancel` of `ask` are called **callback functions** or just **callbacks**.
  - `showOk` becomes the callback for "_yes_" answer, and `showCancel` for "_no_" answer.

> [!tip] Using **Function Expressions** to shorten:
>
> ```javascript
> function ask(question, yes, no) {
>   if (confirm(question)) yes();
>   else no();
> }
>
> ask(
>   "Do you agree?",
>   function () {
>     alert("You agreed.");
>   },
>   function () {
>     alert("You cancelled the execution.");
>   }
> );
> ```
>
> - here, functions are declared inside `ask(...)` call.
> - They have no name, and so are called **anonymous**
>   - Such functions are **_not accessible outside of_** `ask`
>     - because they're not assigned to variables
