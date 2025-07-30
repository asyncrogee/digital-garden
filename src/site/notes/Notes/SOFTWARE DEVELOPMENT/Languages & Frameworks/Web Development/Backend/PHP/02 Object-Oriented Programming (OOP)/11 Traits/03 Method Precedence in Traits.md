---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/11-traits/03-method-precedence-in-traits/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.055+08:00"}
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
