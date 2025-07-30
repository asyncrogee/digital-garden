---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/11-traits/04-method-name-conflict-insteadof/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.050+08:00"}
---


---

> [!caution] `Method` **NAME** conflict between `traits`
> If `traits` are used in a **Class**, and BOTH `traits` have a **METHOD with the SAME NAME**
> It wouldn't know which to run.
>
> **USE `insteadof` to SPECIFY**
>
> ```php
> namespace App;
>
> class AllInOneCoffeeMaker extends CoffeeMaker
> {
> 	use CappuccinoTrait;
>
> 	use LatteTrait {
> 		LatteTrait::makeLatte insteadof CappuccinoTrait;
> 	}
> }
> ```
