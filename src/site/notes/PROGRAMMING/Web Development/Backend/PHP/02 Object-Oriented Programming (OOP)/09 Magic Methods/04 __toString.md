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

Runs when interacting with `Methods` as `String` like **Echo-ing it**

```php
require_once __DIR__ .'/../vendor/autoload.php';

$invoice = new App\Invoice();

echo $invoice;
```

```php
namespace App;

class Invoice;

public function __toString(): string
{
	return 'hello';
}
```

##### Stringable

```php
var_dump($invoice instanceof Stringable);
```

P.S. The code below is not needed if `__toString()` **is already defined**:

```php
class Invoice implements \Stringable
{
	// ...
}
```
