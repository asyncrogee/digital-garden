---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/javascript-vanilla/03-objects/03-garbage-collection/01-reachability/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2025-07-13T15:24:56.508+08:00"}
---


# Reachability

---

The main concept of _memory management_ in JavaScript is **_reachability_**.

"**Reachable**" values are those that are accessible or usable somehow.
They are guaranteed to be stored in memory.

> [!Info] **Roots** > **Roots** are set of inherently reachable values, that **_cannot be deleted_**:
>
> - Currently executing function, its local variables and parameters.
> - Other function on the current chain of nested calls, their local variables and parameters.
> - Global variables
> - (there are some other, internal ones as well)

Any other values is _considered reachable_ if it's reachable from a **root by reference or by a chain of references**.

> [!example]-
> If there's an `object` in a global variable,
> and that `object` has a **property** **_referencing another_** `object`,
> that `object` is considered _reachable_.
> And those **it references** are also _reachable_.

---

> [!example]
>
> ```javascript
> // user has a reference to the object
> let user = {
>   name: "John",
> };
> ```
>
> ![[Pasted image 20240117160540.png]]
> If the values of `user` is **overwritten**, the reference is **_lost_**:
>
> ```javascript
> user = null;
> ```
>
> ![[Pasted image 20240117160646.png]]
> The object becomes unreachable. Garbage collector will junk the data and free the memory.
>
> ## Two References
>
> The object is still reachable via `admin` global variable.
>
> ```javascript
> // user has a reference to the object
> let user = {
>   name: "John",
> };
>
> let admin = user;
> ```
>
> ![[Pasted image 20240117160904.png]]
>
> ```javascript
> user = null;
> ```
>
> If `admin` is also overwritten, then it will be removed.
>
> ## Interlinked objects
>
> The `marry` function "**marries**" two `objects` by giving them references to each other and returns a new `object` that _contains them both_.
>
> ```javascript
> function marry(man, woman) {
>   woman.husband = man;
>   man.wife = woman;
>
>   return {
>     father: man,
>     mother: woman,
>   };
> }
>
> let family = marry(
>   {
>     name: "John",
>   },
>   {
>     name: "Ann",
>   }
> );
> ```
>
> ![[Pasted image 20240117194308.png]]
>
> > [!Danger] Removing two references:
> >
> > ```javascript
> > delete family.father;
> > delete family.mother.husband;
> > ```
> >
> > ![[Pasted image 20240117200046.png]] >> **_Outgoing references_** do not matter.
> > Only **incoming** ones can make an object _reachable_.
> > ![[Pasted image 20240117200541.png]]
> > After garbage collection:
> > ![[Pasted image 20240117201922.png]]
>
> ## Unreachable island
>
> ```javascript
> family = null;
> ```
>
> ![[Pasted image 20240117202413.png]]
> John and Ann still linked (both have incoming references)
> But `family` object has been unlinked from the root, no reference to it any more, so the whole island becomes unreachable and will be removed.

READ MORE:
INTERNAL ALGORITHMS - https://javascript.info/garbage-collection#internal-algorithms
