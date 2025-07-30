---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/01-basics/09-logical-operators/00-examples/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:24:55.994+08:00"}
---

```javascript
let userName = prompt("Who's there?", '');

if (userName === 'Admin') {
  let pass = prompt('Password?', '');

  if (pass === 'TheMaster') {
    alert( 'Welcome!' );
  } else if (pass === '' || pass === null) {
    alert( 'Canceled' );
  } else {
    alert( 'Wrong password' );
  }
  

} else if (userName === '' || userName === null) {
  alert( 'Canceled' );
} else {
  alert( "I don't know you" );
}
```

