---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/03-namespace/04-importing-multiple-classes/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:51.609+08:00"}
---


---

- Including both inside a **Curly braces**:

```php
use PaymentGateway\Paddle\{Transaction, Customer Profile};

$paddleTransaction = new Transaction();
$paddleCustomerProfile = new CustomerProfile();
```

- Or just straight importing the `namespace`:

```php
use PaymentGateway\Paddle;

$paddleTransaction = new Paddle\Transaction();
$paddleCustomerProfile = new Paddle\CustomerProfile();
```
