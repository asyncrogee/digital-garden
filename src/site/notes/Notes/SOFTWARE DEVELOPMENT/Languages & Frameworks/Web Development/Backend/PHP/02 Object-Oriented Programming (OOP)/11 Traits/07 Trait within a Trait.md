---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/11-traits/07-trait-within-a-trait/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.038+08:00"}
---


---

```php
namespace App;

trait CappuccinoTrait
{
	use LatteTrait; // Using another Trait

	private function makeCappuccino()
	{
		// ...
	}
}
```
