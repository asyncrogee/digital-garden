---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/03-objects/01-objects-basics/03-property-value-shorthand/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


# Property value shorthand

---

```javascript
function makeUser(name, age) {
  return {
    name: name,
    age: age,
    // ...other properties
  };
}

let user = makeUser("John", 30);
alert(user.name); // John
```

> [!tip] Special property shorthand
> Instead of `name:name` we can just write `name` like this:
>
> ```javascript
> function makeUser(name, age) {
>   return {
>     name, // same as name: name
>     age, // same as age: age
>     // ...
>   };
> }
> ```
>
> Using both _normal_ and **shorthand** properties in the same object:
>
> ```javascript
> let user = {
>   name, // same as name:name
>   age: 30,
> };
> ```
