---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/15-object-cloning-and-clone-magic-method/01-clone-and-magic/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.113+08:00"}
---


---

### Clone

```php
$invoice = new \App\Invoice();

$invoice2 = clone $invoice;

var_dump($invoice, $invoice2, $invoice === $invoice2);
```

**_OUTPUT_**:
![[Pasted image 20240330023527.png]]

- `clone` **SHALLOW COPY** the `properties`
- and also **COPY THE `ID`**
- but THEY ARE STILL **DIFFERENT `OBJECTS`**

### Magic Clone Method

```php
namespace App;

class Invoice
{
	private string $id;

	public function __construct()
	{
		$this->id = uniqid('invoice_');
		var_dump('__construct');
	}

	public function __clone(): void
	{
		$this->id = uniqid('invoice_');
		var_dump('__clone');
	}
}
```

**_OUTPUT_**:
![[Pasted image 20240330024321.png]]

- `__construct()` **DOESN'T GET CALLED** when `clone` is runned.
