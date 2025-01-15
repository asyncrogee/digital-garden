---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/04-interaction-alert-prompt-confirm/03-confirm/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:41.656+08:00"}
---


# 03 confirm

---

```javascript
result = confirm(question);
```

The function **_confirm_** shows a modal window with a **question** and two buttons: OK and Cancel

The result is **_true_** if OK is pressed
and **_false_** otherwise.

example:

```javascript
let isBoss = confirm("Are you the boss?");

alert(isBoss);
```
