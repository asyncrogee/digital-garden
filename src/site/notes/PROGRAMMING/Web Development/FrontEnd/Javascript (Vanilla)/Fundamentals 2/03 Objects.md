---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/fundamentals-2/03-objects/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:42.607+08:00"}
---


# 03 Objects

---

> [!info] Objects
>
> - Can be created with figure brackets `{...}` with an optional list of properties
> - Property - "**key: value**" pair, where `key` is a _string_ (aka "**_property name_**")
> - `value` can be **anything**
>
> ```javascript
> const jonas = {
> 	firstName: 'Jonas',
> 	lastName: 'Schmedtmann'
> 	age: 2037 - 1991,
> 	job: 'teacher'
> 	friends: ['Michael', 'Peter', 'Steven']
> };
> ```

> [!abstract] Empty Object
> Empty object can be created using these two syntax:
>
> ```javascript
> let user = new Object(); // "object constructor" syntax
> let user = {}; // "object literal" syntax
> ```

> [!tip] Multiword Property Names
> Multiword Property name **must be quoted**
>
> ```javascript
> let user = {
>   name: "John",
>   age: 30,
>
>   "likes birds": true,
> };
> ```

> [!tip] Adding new properties
> Dot Notation:
>
> ```javascript
> objectName.propertyName = Value;
>
> jonas.location = "Portugal";
> ```
>
> Square Brackets:
>
> ```javascript
> objectName['propertyName'] = value;
>
> jonas['twitter'] = @jonasschmedtman;
> ```

```

```

```

```

> [!tip] Last property in the list **may end with a comma**:
>
> ```javascript
> let user = {
>   name: "John",
>   age: 30,
> };
> ```

---

## Accessing Objects

> [!tip] Dot Notation
>
> ```javascript
> alert(user.name);
> alert(user.age);
> ```
>
> Adding a boolean value:
>
> ```javascript
> user.isAdmin = true;
> ```
>
> Remove a property:
>
> ```javascript
> delete user.age;
> ```

> [!caution] Dot Multiword properties
> Dot access doesn't work with Multiword properties
>
> ```javascript
> // this would give a syntax error
> user.likes birds = true
> ```
>
> Dot requires the key to be a **valid variable identifier**.
>
> - Contains no spaces
> - Doesn't start with a _digit_
> - doesn't include special characters (`$` and `_` are allowed).

> [!tip] Square brackets Notation
> Works with any string
>
> ```javascript
> let user = {};
>
> // set
> user["likes birds"] = true;
>
> //get
> alert(user["likes birds"]); // true
>
> // delete
> delete user["likes birds"];
> ```
>
> ```javascript
> let key = "likes birds";
>
> // same as user["likes birds"] = true;
> user[key] = true;
> ```
>
> ```javascript
> let user = {
>   name: "John",
>   age: 30,
> };
>
> let key = prompt("What do you want to know about the user?", "name");
>
> // access by variable
> alert(user[key]); // John (if enter "name")
> ```

---

### More examples:

```javascript
const jonas = {
  firstName: "Jonas",
  lastName: "Schmedtmann",
  age: 2037 - 1991,
  job: "teacher",
  friends: ["Michael", "Peter", "Steven"],
};

const interestedIn = prompt(
  "What do you want to know about Jonas? Choose between firstName, lastName, age, job, and friends"
);

if (jonas[interestedIn]) {
  console.log(jonas[interestedIn]);
} else {
  console.log(
    "Wrong request! What do you want to know about Jonas? Choose between firstName, lastName, age, job, and friends"
  );
}
```

```javascript
const jonas = {
  firstName: "Jonas",
  lastName: "Schmedtmann",
  age: 2037 - 1991,
  job: "teacher",
  friends: ["Michael", "Peter", "Steven"],
};

console.log(
  `${jonas.firstName} has ${jonas.friends.length} friends, and his best friend is called ${jonas.friends[0]}`
);
```
