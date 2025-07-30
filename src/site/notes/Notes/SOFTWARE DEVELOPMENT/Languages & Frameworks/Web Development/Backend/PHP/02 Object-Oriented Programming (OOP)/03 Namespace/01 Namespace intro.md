---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/03-namespace/01-namespace-intro/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:51.617+08:00"}
---


---

> [!caution]
> When declaring a `variable`, `constant`, `functions`, or `classes`, It automatically stores in the **_Global scope_**.
>
> - This could result to an **_ERROR_** when `names` are used more than once.

> [!info] NameSpace
>
> - Is like a **Virtual Directories**
> - Groups `variable`, `constant`, `function` and `classes`

> [!example]
>
> ```php
> declare(strict_types = 1);
>
> namespace Bayaran;
>
> class Transaction
> {
>
> }
> ```
>
> _In another file_:
>
> ```php
> require_once '.../PaymentGateway/Paddle/Transaction.php';
>
> var_dump(new Bayaran\Transaction);
> ```
>
> ---
>
> ---
>
> ---
>
> ```php
> declare(strict_types = 1);
>
> namespace PaymentGateway\Stripe;
>
> class Transaction
> {
>
> }
> ```
>
> ```php
> declare(strict_types = 1);
>
> namespace PaymentGateway\Paddle;
>
> class Transaction
> {
> }
> ```
>
> ```php
> require_once '.../PaymentGateway/Stripe/Transaction.php'
> require_once '.../PaymentGateway/Paddle/Transaction.php'
> require_once '.../PaymentGateway/Paddle/CustomerProfile.php'
>
> var_dump(new PaymentGateway\Strip\Transaction());
> ```

> [!tip] `use` keyword to Import `namespace`
>
> ```php
> require_once '.../PaymentGateway/Stripe/Transaction.php'
> require_once '.../PaymentGateway/Paddle/Transaction.php'
>
> use PaymentGateway\Stripe\Transaction;
>
> new Transaction();
> ```
