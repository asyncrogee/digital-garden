---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/11-traits/01-problem/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.063+08:00"}
---


---

> [!caution] Diamond Problem
> ![[Pasted image 20240329080559.png]]
>
> - `All in One Coffee Maker` doesn't know **WHICH `makeCoffee` METHOD TO RUN**

_CoffeeMaker.php_

```php
namespace App;

class CoffeeMaker
{
	public function makeCoffee()
	{
		echo static::class . ' is making coffee' . PHP_EOL;
	}
}
```

_LatteMaker.php_

```php
namespace App;

class LatteMaker extends CoffeeMaker
{
	public function makeLatte()
	{
		echo static::class . ' is making latte' . PHP_EOL;
	}
}
```

_CappuccinoMaker.php_

```php
namespace App;

class CappuccinoMaker extends CoffeeMaker
{
	public function makeCapuccino()
	{
		echo static::class . ' is making cappucino' . PHP_EOL;
	}
}
```

_AllInOneCoffeeMaker.php_

```php
namespace App;

class AllInOneCoffeeMaker
{

}
```

_Index.php_

```php
$coffeeMaker = new \App\CoffeeMaker();
$coffeeMaker->makeCoffee();

$latteMaker = new \App\LatteMaker();
$latteMaker->makeCoffee();
$latteMaker->makeLatte();
```

---

##### **Interfaces** instead of **_Multiple Inheritance_**

- **Interfaces** is GOOD if the _IMPLEMENTATION IS DIFFERENT_
- NOT when you only **_DUPLICATING_** the `code`
  _AllInOneCoffeeMaker.php_

```php
namespace App;

class AllInOneCoffeeMaker extends CoffeeMaker implements MakesLatte, MakesCappuccino
{
	public function makeLatte()
	{
		echo static::class . ' is making latte' . PHP_EOL;
	}

	public function makeCapuccino()
	{
		echo static::class . ' is making cappucino' . PHP_EOL;
	}
}
```

_Index.php_

```php
$coffeeMaker = new \App\CoffeeMaker();
$coffeeMaker->makeCoffee();

$latteMaker = new \App\LatteMaker();
$latteMaker->makeCoffee();
$latteMaker->makeLatte();
```
