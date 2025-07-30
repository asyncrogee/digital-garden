---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/09-magic-methods/04-to-string/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.980+08:00"}
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
