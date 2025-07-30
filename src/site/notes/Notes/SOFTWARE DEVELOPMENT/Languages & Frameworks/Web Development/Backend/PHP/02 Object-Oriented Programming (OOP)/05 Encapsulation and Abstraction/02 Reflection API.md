---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/05-encapsulation-and-abstraction/02-reflection-api/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.879+08:00"}
---


---

Accessing the **Private** and **Protected** `Properties` or `Methods`

```php
use App\PaymentGateway\Paddle\Transaction;

require_once __DIR__ . '/../vendor/autoload.php';

$transaction = new Transaction(25);

$reflectionProperty = new ReflectionProperty(Transaction::class, 'amount');

$reflectionProperty->setAccessible(true);

// Accessed the Private Property
var_dump($reflectionProperty->getValue($transaction)); // float(25)

//Modifying the Private Property
$reflectionProperty->setValue($transaction, 125);
var_dump($reflectionProperty->getValue($transaction)); // float(125)

```
