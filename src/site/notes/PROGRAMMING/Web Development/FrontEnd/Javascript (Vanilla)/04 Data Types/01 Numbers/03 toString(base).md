---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/04-data-types/01-numbers/03-to-string-base/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:33.271+08:00"}
---


---

# toString(base)

---

> [!abstract]
> method `num.toString(base)` returns a **string representation** of `num` in the numeral system with the given `base`.
>
> ```javascript
> let num = 255;
>
> alert(num.toString(16)); // ff
> alert(num.toString(2)); // 11111111
> ```
>
> `base` can vary from `2` to `36`
> By default it's `10`
>
> > [!tip] Common use cases:
> >
> > - `base = 16` used for **hex colors**, **character encodings** etc, digits can be `0..9` or `A..F`
> > - `base = 2` mostly for **debugging bitwise operations**, digits can be `0` or `1`
> > - `base = 36` **the maximum**, digits can be `0..9` or `A..Z`.
> >   - Useful case: Turning a **long numeric identifier** into something shorter.
> >     - For Example: Make a **_Short URL_**.
> >
> > > [!example] `base = 36` Example
> > >
> > > ```javascript
> > > alert((123456).toString(36)); // 2n9c
> > > ```

> [!tip] 2 dots e.g. `..toString()`
> To call a method **directly on a number**, like `toString` then we **need to place two dots** `..` after it.
>
> Placing a **_single dot_** would cause an error: `123456.toString(36)`
> JavaScript implies the **_decimal part_** after the **_first dot_**.
>
> So, **if we place more dots**, JavaScript knows that the **_decimal part_** is **empty** and now goes the **method**.
>
> Could also write `(123456).toString(36)`
