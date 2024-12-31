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
