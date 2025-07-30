---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/11-traits/06-method-visibility/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.042+08:00"}
---


---

> [!tip] Change **Visibility** of `trait methods`
> Setting a **Trait** `method` private or protected,
> **CAN STILL BE USED by the `Class` that uses that `Trait`**
> but, NOT OUTSIDE OF IT.
>
> ---
>
> - Change it's `visibility`
>
> ```php
> class CappuccinoMaker extends CoffeeMaker
> {
> 	use CappuccinoTrait {
> 		CappuccinoTrait::makeCappuccino as public;
> 	}
> }
> ```
