---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/03-objects/07-symbol-type/01-symbols/","tags":["programming","webdevelopment","frontend","JavaScript"]}
---


## Symbol Type

---

> [!abstract] #### Symbol type
> Only **two primitive types** may serve as object property keys:
>
> - **STRING** type, or
> - **SYMBOL** type
>
> **_Any other types_** are automatically converted to `string`.
>
> - `obj[1]` equals `obj["1"]`
> - `obj[true]` equals `obj["true"]`

> [!tip] Summary:
>
> - `Symbol()` are like **unofficial property** of an `object`.
> - Not written directly, but associates itself to the `object`. (Like adopted itself to the `object`).
> - Each `Symbol()` has **unique id** even if they have the **_same description_**.
> - **Only accessible in the file where it's created/it's scope**.

> [!info] #### Symbols
> A **"symbol"** represents a unique identifier.
>
> Can be created using `Symbol()`:
>
> ```javascript
> let id = Symbol();
> ```
>
> > [!tip] Symbol Name
> > Symbols can be given a description, useful for debugging
> >
> > ```javascript
> > // id is a symbol with the description "id"
> > let id = Symbol("id");
> > ```
> >
> > - **Symbols are UNIQUE**
> > - Symbols with the **_same description_** are different.
> > - The `description` is just a **label** that **doesn't affect anything**.
> >
> > ```javascript
> > let id1 = Symbol("id");
> > let id2 = Symol("id");
> >
> > alert(id1 == id2); // false
> > ```
> >
> > > [!danger] Symbols don't auto-convert to a string
> > > `alert` converts almost any value.
> > > **Symbols** don't auto-convert.
> > >
> > > ```javascript
> > > let id = Symbol("id");
> > > alert(id); // TypeError: Cannot convert a Symbol value to a string
> > > ```
> > >
> > > > [!done] Show **Symbol**:
> > > >
> > > > - `toString()`:
> > > >
> > > > ```javascript
> > > > let id = Symbol("id");
> > > > alert(id.toString()); // Symbol(id), now it works
> > > > ```
> > > >
> > > > - `symbol.description`
> > > >
> > > > ```javascript
> > > > let id = Symbol("id");
> > > > alert(id.description); // id
> > > > ```
