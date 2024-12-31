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
