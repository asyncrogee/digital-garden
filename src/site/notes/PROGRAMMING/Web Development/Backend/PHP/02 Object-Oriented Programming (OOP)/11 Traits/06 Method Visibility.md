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
