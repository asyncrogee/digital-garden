---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/11-traits/05-method-nickname-as/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.046+08:00"}
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
