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
