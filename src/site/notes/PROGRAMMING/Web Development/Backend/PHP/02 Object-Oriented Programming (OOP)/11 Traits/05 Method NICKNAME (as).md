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

> [!TIP] Ali`as`
> Set a _nickname_ for `trait methods`
>
> ```php
> namespace App;
>
> class AllInOneCoffeeMaker extends CoffeeMaker
> {
> 	use CappuccinoTrait ;
>
> 	use LatteTrait {
> 		LatteTrait::makeLatte as makeOriginalLatte;
> 	}
> }
> ```
