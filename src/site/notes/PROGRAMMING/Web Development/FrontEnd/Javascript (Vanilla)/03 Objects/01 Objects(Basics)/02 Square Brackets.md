---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/03-objects/01-objects-basics/02-square-brackets/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:39.427+08:00"}
---


# Square Brackets

---

Dot access won't work for **multiword properties**

```javascript
// this would give a syntax error
user.likes birds = true
```

- JavaScript thinks that we address `user.likes`
- then gives syntax error when comes across unexpected `birds`

**DOT** requires valid variable indentifiers

- Contains **no spaces**
- doesn't start with a **digit**
- Doesn't include special characters (`$` and `_` are allowed).

## Square bracket notation

Square brackets are much more powerful than dot notation.
They allow any property names and variables.
Words with any string:

- _String_ inside the brackets is properly `quoted` (any type of quotes).

```javascript
let user = {};

// set
user["likes birds"] = true;

// get
alert(user["likes birds"]); // true

// delete
delete user["likes birds"];
```

Square brackets are also use to obtain `property name` as the result of _any expression_:

```javascript
let key = "likes birds";

// same as user["likes birds"] = true;
user[key] = true;
```

```javascript
let user = {
  name: "John",
  age: 30,
};

let key = prompt("What do you want to know about the user?", "name");

// access by variable
alert(user[key]); // John (if enter "name")
```

`Dot notation` **cannot be used** in a similar way:

```javascript
let user = {
  name: "John",
  age: 30,
};
let key = "name";
alert(user.key); // undefined
```

## Computer properties

```javascript
let fruit = prompt("Which fruit to buy?", "apple");

let bag = {
  [fruit]: 5, // the name of the property is taken from the variable fruit
};

alert(bag.apple); // 5 if fruit="apple"
```

works the same as:

```javascript
let fruit = prompt("Which fruit to buy?", "apple");
let bag = {};

bag[fruit] = 5;
```

```javascript
let fruit = "apple";
let bag = {
  [fruit + "Computers"]: 5, // bag.appleComputers = 5
};
```
