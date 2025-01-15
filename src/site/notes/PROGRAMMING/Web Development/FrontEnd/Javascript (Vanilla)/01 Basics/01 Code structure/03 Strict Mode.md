---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/01-code-structure/03-strict-mode/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:41.978+08:00"}
---


# 03 Strict Mode

---

```javascript
"use script";

// the code works the modern way
```

`"use strict"` can be enabled in a **function only**, by putting it in the beginning of a function.

> [!caution] Ensure that `"use strict"` is at the top
> **Strict mode** will not enable, if its not on top of the script
>
> ```javascript
> alert("some code");
> // "use strict" below is ignored -- it must be at the top
>
> ("use strict");
>
> // strict mode is not activated
> ```
>
> - Only _comments_ appear above `"use strict"`

> [!tip]
>
> - Strict mode helps us by giving more information about bugs and errors.
> - Strict mode reserves certain keywords that we can't use as variables, such as:
>   - `interface`
>   - `private`
>   - etc.
