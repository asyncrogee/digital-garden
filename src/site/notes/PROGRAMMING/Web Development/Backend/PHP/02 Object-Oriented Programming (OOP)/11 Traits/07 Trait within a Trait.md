---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/02-object-oriented-programming-oop/11-traits/07-trait-within-a-trait/","tags":["programming","php","webdevelopment","backend","OOP"]}
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
