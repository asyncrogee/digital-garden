---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/11-traits/08-properties-within-traits/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.034+08:00"}
---


---

- `Property` inside a **Trait** can be used:
  - IN THE **TRAIT**
  - and the `Class` that uses the **Trait**

```php
namespace App;

trait LatteTrait
{
	protected string $milkType = 'whole-milk';

	public function makeLatte()
	{
		echo static::class . ' is making latte with' . $this->milkType . PHP_EOL;
	}
}
```

> [!example]
> In some code, others use `properties` **_not defined_** inside the `trait`
> like doing `$this->milkType` **WITHOUT DEFINING** it inside the `trait`
>
> _Trait File_:
>
> ```php
> namespace App;
>
> trait LatteTrait
> {
> 	public function makeLatte()
> 	{
> 		echo static::class . ' is making latte with ' . $this->milkType . PHP_EOL;
> 	}
> }
> ```
>
> _Class that uses the Trait above_:
>
> ```php
> namespace App;
>
> class LateMaker extends CoffeeMaker
> {
> 	use LatteTrait;
>
> 	private string $milkType = 'whole-milk';
> }
> ```
