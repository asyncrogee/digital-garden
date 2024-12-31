---
ProgrammingLanguage: PHP
tags:
  - programming
  - php
  - webdevelopment
  - backend
  - OOP
dg-publish: true
Topic: OOP
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
