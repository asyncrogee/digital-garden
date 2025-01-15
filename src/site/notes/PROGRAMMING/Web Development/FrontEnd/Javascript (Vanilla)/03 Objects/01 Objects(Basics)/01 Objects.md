---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/03-objects/01-objects-basics/01-objects/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:39.474+08:00"}
---


# Objects

---

> [!info] Object
> Objects are used to store keyed collections of various data and more complex entities.
>
> - Created with figure brackets `{...}` with an optional list of properties.
>   - A property is a "**key:value**" pair,
>   - where `key` is a _string_ (aka "**property name**"),
>   - `value` can be **anything**.
>
> ```javascript
> let user = {
>   // an object
>   name: "John", // by key "name" store value "John"
>   age: 30, // by key "age" store value 30
> };
> ```
>
> `user` object has two properties:
>
> 1. First has the name "`name`" and value "`John`".
> 2. Second has the name "`age`" and value "`30`".
>
> > [!tip] Add, Remove and Read files any time.
> >
> > - **READ**:
> >
> > ```javascript
> > // get property values of the object:
> > alert(user.name); // John
> > alert(user.age); // 30
> > ```
> >
> > - **ADD**:
> >
> > ```javascript
> > user.isAdmin = true;
> > ```
> >
> > ![Pasted image 20240112192338.png](/img/user/PROGRAMMING/Web%20Development/FrontEnd/Javascript%20(Vanilla)/03%20Objects/attachments/Pasted%20image%2020240112192338.png)
> >
> > - **DELETE**:
> >
> > ```javascript
> > delete user.age;
> > ```
> >
> > ![Pasted image 20240112192354.png](/img/user/PROGRAMMING/Web%20Development/FrontEnd/Javascript%20(Vanilla)/03%20Objects/attachments/Pasted%20image%2020240112192354.png)
>
> > [!TIP] Multiword Property names:
> > _Multiword Property_ mush be **quoted**.
> >
> > ```javascript
> > let user = {
> >   name: "John",
> >   age: 30,
> >   "likes birds": true, // multiword property name must be quoted
> > };
> > ```
> >
> > ![Pasted image 20240112192631.png](/img/user/PROGRAMMING/Web%20Development/FrontEnd/Javascript%20(Vanilla)/03%20Objects/attachments/Pasted%20image%2020240112192631.png)
>
> > [!tip] **"Trailing"** or **"Hanging"** comma.
> > Makes it easier to add/remove/move around properties, because all lines become alike.
> > The last property in the list may end with a comma:
> >
> > ```javascript
> > let user = {
> >   name: "John",
> >   age: 30,
> > };
> > ```
