---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/03-objects/07-symbol-type/02-hidden-properties/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


# Design

---

> [!abstract] "Hidden" property
> Symbols allow us to **create “hidden” properties of an object**, that no other part of code can accidentally access or overwrite.
>
> > [!example]
> > Working with `user` objects **that belong to a third-party code**.
> >
> > ```javascript
> > let user = {
> >   // belongs to another code
> >   name: "John",
> > };
> >
> > let id = Symbol("id");
> >
> > user[id] = 1;
> >
> > alert(user[id]); // we can access the data using the symbol as the key
> > ```
>
> > [!tip] Benefit of using `Symbol("id")` over _string_ `"id"`
> > If the `object` **belongs to another codebase**, Using `Symbol()` will **_not affect the original_** `object`.
> > The new `Symbol()` property is only accessible where it's created.
> >
> > Meanwhile, using **string** `"id"` or **property** **_affect the original codebase_** or `object`.
