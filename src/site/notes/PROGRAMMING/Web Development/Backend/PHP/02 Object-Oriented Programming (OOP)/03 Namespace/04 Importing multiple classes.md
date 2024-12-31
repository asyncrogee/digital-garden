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
