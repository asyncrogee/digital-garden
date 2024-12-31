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

> [!tip] METHOD PRECEDENCE
>
> 1. **Class** `method`
> 2. **Trait** `method`
> 3. **Parent Class** `method`
>
> ```php
> class CappucinoMaker extends CoffeeMaker
> {
> 	use CappuccinoTrait; // also has makeCappuccino() method
>
> 	public function makeCappuccino()
> 	{
> 		echo 'Making Cappuccino (UPDATED)' . PHP_EOL;
> 	}
> }
> ```
