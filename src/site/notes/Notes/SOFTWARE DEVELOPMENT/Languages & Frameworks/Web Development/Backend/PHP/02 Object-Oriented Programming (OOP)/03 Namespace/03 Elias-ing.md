---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/03-namespace/03-elias-ing/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:51.614+08:00"}
---


---

```php
use theNameofNamespace as theElias;
```

```php
require_once '../PaymentGateway/Stripe/Transactio.php';
require_once '../PaymentGateway/Paddle/Transactio.php';

use PaymentGateway\Paddle\Transaction;
use PaymentGateway\Stripe\Transaction as StripeTransaction;

$paddleTransaction = new Transaction();
$stripeTransaction = new StripeTransaction();

var_dump($paddleTransaction, $stripeTransaction);
```

another example:

```php
declare(strict_types = 1);

namespace PaymentGateway\Paddle;

use VendorName\Transaction as VendorTransaction;

class Transaction
{
	public function __construct()
	{
	}
}
```
