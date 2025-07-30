---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/11-traits/10-static-properties-and-methods-in-traits/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.026+08:00"}
---


---

> [!info]
>
> ```php
> namespace App;
>
> trait LatteTrait
> {
> 	public static int $x = 1;
>
> 	public static function foo()
> 	{
> 		echo 'Foo Bar' . PHP_EOL;
> 	}
>
> }
> ```
>
> ```php
> \App\LatteMaker::foo();
> echo \App\LatteMaker:: $x;
> ```
