---
ProgrammingLanguage: PHP
tags:
  - programming
  - php
  - webdevelopment
  - backend
  - OOP
dg-publish: true
Topic: OOP
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
![Pasted image 20240329061117.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/09%20Magic%20Methods/attachments/Pasted%20image%2020240329061117.png)
