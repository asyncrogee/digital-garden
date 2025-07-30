---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/09-magic-methods/06-debug-info/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.974+08:00"}
---


---

Return a `null` or an `array`

###### Problem:

```php
require_once __DIR__ . '/../vendor/autload.php';

$invoice = new App\Invoice();

var_dump($invoice);
```

```php
namespace App;

class Invoice
{
	private float $amount;
	private int $id;
	private string $accountNumber;
}
```

- This prints out **EVERY `PROPERTY`** of the `CLASS`
  - **_EVEN THE `PRIVATE` ONCE_**

---

We can specify **WHICH TO RETURN** using `__debuginfo`

```php
namespace App;

class Invoice
{
	private float $amount;
	private int $id = 1;
	private string $accountNumber = '0123456789';

	public function __debugInfo(): ?array
	{
		return [
			'id' => $id,
			'accountNumber' => '****' . substr($this->accountNumber, -4),
		];
	}
}
```

```php
require_once __DIR__ . '/../vendor/autload.php';

$invoice = new App\Invoice();

var_dump($invoice);
```

**OUTPUT**:
![[Pasted image 20240329061117.png]]
