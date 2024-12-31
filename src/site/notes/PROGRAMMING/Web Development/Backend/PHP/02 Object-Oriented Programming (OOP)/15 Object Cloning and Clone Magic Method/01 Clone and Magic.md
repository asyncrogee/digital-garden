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

### Clone

```php
$invoice = new \App\Invoice();

$invoice2 = clone $invoice;

var_dump($invoice, $invoice2, $invoice === $invoice2);
```

**_OUTPUT_**:
![Pasted image 20240330023527.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/15%20Object%20Cloning%20and%20Clone%20Magic%20Method/attachments/Pasted%20image%2020240330023527.png)

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
![Pasted image 20240330024321.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/15%20Object%20Cloning%20and%20Clone%20Magic%20Method/attachments/Pasted%20image%2020240330024321.png)

- `__construct()` **DOESN'T GET CALLED** when `clone` is runned.
