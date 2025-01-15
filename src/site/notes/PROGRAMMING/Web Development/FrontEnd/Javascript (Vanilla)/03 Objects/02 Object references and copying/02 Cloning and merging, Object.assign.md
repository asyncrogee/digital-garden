---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/03-objects/02-object-references-and-copying/02-cloning-and-merging-object-assign/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:39.412+08:00"}
---


# Cloning and merging

---

> [!info]- Summary
> Objects are assigned and copied by **reference**.
> In other words, a variable stores not the “object value”, but a “reference” (address in memory) for the value.
> So copying such a variable or passing it as a function argument copies that reference, **not the object itself**.
>
> All operations via copied references (like adding/removing properties) are performed on the same single object.
>
> To make a “**real copy**” (a clone) we can use `Object.assign` for the so-called “**shallow copy**” (nested objects are copied by reference) or a “**deep cloning**” function `structuredClone` or use a custom cloning implementation, such as [\_.cloneDeep(obj)](https://lodash.com/docs#cloneDeep).

Duplicating an object:

```javascript
let user = {
  name: "John",
  age: 30,
};

let clone = {}; // the new empty object

// let's copy all user properties into it
for (let key in user) {
  clone[key] = user[key];
}

// now clone is a fully independent object with the same content
clone.name = "Pete"; // changed the data in it

alert(user.name); // still John in the original object
```

> [!tip] `Object.assign`
>
> > [!info] Syntax:
> >
> > ```javascript
> > Object.assign(dest, ...sources);
> > ```
> >
> > - First argument / `dest` is a **target object**.
> > - Further arguments is a list of _source objects_
> >   It **copies all the `properties` of all source objects** into the target `dest`, and then returns it as the result.
>
> Example:
>
> ```javascript
> let user = { name: "John" };
>
> let permissions1 = { canView: true };
> let permissions2 = { canEdit: true };
>
> // copies all properties from permissions1 and permissions2 into user
> Object.assign(user, permissions1, permissions2);
>
> // now user = { name: "John", canView: true, canEdit: true }
> alert(user.name); // John
> alert(user.canView); // true
> alert(user.canEdit); // true
> ```
>
> > [!tip] If copied property name _already exists_, it gets **overwritten**:
> >
> > ```javascript
> > let user = { name: "John" };
> >
> > Object.assign(user, { name: "Pete" });
> >
> > alert(user.name); // now user = { name: "Pete" }
> > ```
>
> > [!important] Simple object cloning using `Object.assign`
> >
> > ```javascript
> > let user = {
> >   name: "John",
> >   age: 30,
> > };
> >
> > let clone = Object.assign({}, user);
> >
> > alert(clone.name); // John
> > alert(clone.age); // 30
> > ```

> [!danger] Nested Cloning
> Properties can be references to _other objects_.
>
> ```javascript
> let user = {
>   name: "John",
>   sizes: {
>     height: 182,
>     width: 50,
>   },
> };
>
> alert(user.sizes.height); // 182
> ```
>
> `user.sizes` is an object, and will be copied by reference:
>
> ```javascript
> let user = {
>   name: "John",
>   sizes: {
>     height: 182,
>     width: 50,
>   },
> };
>
> let clone = Object.assign({}, user);
>
> alert(user.sizes === clone.sizes); // true, same object
>
> // user and clone share sizes
> user.sizes.width = 60; // change a property from one place
> alert(clone.sizes.width); // 60, get the result from the other one
> ```
>
> > [!done] structuredClone
> > `structuredClone(Object)` clones the `object` with all nested properties.
> > `structuredClone` method can clone most data types, such as `objects`, `arrays`, `primitive values`.
> >
> > ```javascript
> > let user = {
> >   name: "John",
> >   sizes: {
> >     height: 182,
> >     width: 50,
> >   },
> > };
> >
> > let clone = structuredClone(user);
> >
> > alert(user.sizes === clone.sizes); // false, different objects
> >
> > // user and clone are totally unrelated now
> > user.sizes.width = 60; // change a property from one place
> > alert(clone.sizes.width); // 50, not related
> > ```
> >
> > > [!tip] Circular References
> > > When an object property references the **object itself** (directly or via a chain or references).
> > >
> > > ```javascript
> > > let user = {};
> > > // let's create a circular reference:
> > > // user.me references the user itself
> > > user.me = user;
> > >
> > > let clone = structuredClone(user);
> > > alert(clone.me === clone); // true
> > > ```
> > >
> > > - `clone.me` references the `clone`, not the `user`, So the circular reference was cloned correctly as well.
> >
> > > [!caution] There are cases when `structuredClone` fails.
> > > When an object has a **function** property:
> > >
> > > ```javascript
> > > // error
> > > structuredClone({
> > >   f: function () {},
> > > });
> > > ```
> > >
> > > - Function properties **aren't supported**
