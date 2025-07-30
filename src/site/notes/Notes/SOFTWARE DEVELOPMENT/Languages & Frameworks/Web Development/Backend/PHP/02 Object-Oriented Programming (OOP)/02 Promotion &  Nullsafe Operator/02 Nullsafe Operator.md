---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/02-promotion-and-nullsafe-operator/02-nullsafe-operator/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:51.578+08:00"}
---


---

- Prevents **_ERRORS_** when chaining `properties` and `methods` even 1 of them is `NULL`
- When a `property` or `method` is `NULL`, it automatically **discards** everything next to it(or to the right)
  > [!note]- the `Codes` for the example below
  >
  > - _Customer.php_
  >
  > ```php
  > class Customer
  > {
  > 	public ?PaymentProfile $paymentProfile = null;
  > }
  > ```
  >
  > - _PaymentProfile.php_
  >
  > ```php
  > class PaymentProfile
  > {
  > 	public int $id;
  >
  > 	public function __construct()
  > 	{
  > 		$this->id = rand();
  > 	}
  > }
  > ```
  >
  > - _Transaction.php_
  >
  > ```php
  > declare(strict_types = 1);
  >
  > class Transaction
  > {
  > 	public ?Customer $customer = null;
  >
  > 	public function __construct(
  > 		private float $amount,
  > 		private string $description
  > 	) {
  >
  > 	}
  > }
  > ```

Makes `customer` **Nullsafe**:

```PHP
$transaction->customer?->paymentProfile->id;

$transaction->getCustomer()?->getPaymentProfile()?->id;
```

> [!tip] Using `Null Coelscing` Instead
> `Null Coelscing` could work,
>
> ```php
> $transaction->customer->paymentProfile->id ?? 'foo';
> ```
>
> but it WON'T WORK with `methods`
>
> ```php
> $transaction->getCustomer()->getPaymentProfile()->id ?? 'foo';
> ```
