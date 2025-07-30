---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/09-magic-methods/05-invoke/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.977+08:00"}
---


---

Triggered when you try to **Call the `object` directly**

```php
namespace App;

class Invoice
{
	public function __invoke()
	{
		var_dump('invoked');
	}
}
```

- Useful for **SINGLE ACTION `CLASSES`** or **SINGLE RESPONSIBILITY `CLASSES`**

```PHP
class ProcessInvoice
{
	public function __invoke()
	{
		var_dump('invoked');
	}
}
```

- this only serves one purpose, to process the invoice
