---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/04-interaction-alert-prompt-confirm/02-prompt/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


# 02 prompt

---

the Function **prompt** accepts two arguments:

```javascript
result = prompt(title, [default])
```

shows a modal window with a text message, an input field for the visitor, and the buttons OK/Cancel.

**_title_** - text to show the visitor.
**_default_** - optional second parameter, the initial value for the input field

Square brackets means the parameter is **optional, not required**

```javascript
let age = prompt("How old are you?", 100);

alert(`You are ${age} years old!`); // You are 100 years old!
```

- Visitor can type something in the prompt input field and press OK
  - they can cancel the input by pressing Cancel or hitting `ESC`
  - then, we get **_null_** as the result.\_\_
