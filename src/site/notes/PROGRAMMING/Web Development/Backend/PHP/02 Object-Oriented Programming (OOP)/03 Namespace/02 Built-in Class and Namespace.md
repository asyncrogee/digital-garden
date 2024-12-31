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

> [!caution] Same name as a `Built-in Class`
> If you have a `class` with the **SAME NAME** as a `Built-in Class`,
> It would get the **_local_** `class` that you created.

> [!tip] Import from `GLOBAL` not **_Local Namespace_**
>
> ```php
> declare(strict_types = 1);
>
> namespace PaymentGateway\Paddle;
>
> class Transaction
> {
> 	public function __construct()
> 	{
> 		var_dump(new \DateTime());
> 	}
> }
> ```
>
> - add a _Backslash_ (`\`) like `\DateTime()`
>
> Another Way:
>
> - Using `use` keyword, Instead of _backslash_
>
> ```php
> declare(strict_types = 1);
>
> namespace PaymentGateway\Paddle;
>
> use DateTime;
>
> class Transaction
> {
> 	public function __construct()
> 	{
> 		var_dump(new DateTime());
> 	}
> }
> ```

> [!tip] Importing from other folder
> Two ways:
>
> 1. _Backslash_ before it
>
> ```php
> declare(strict_types = 1);
>
> namespace PaymentGateway\Paddle;
>
> use DateTime;
>
> class Transaction
> {
> 	public function __construct()
> 	{
> 		var_dump(new \Notification\Email());
> 	}
> }
> ```
>
> 2. `use` keyword:
>
> ```php
> declare(strict_types = 1);
>
> namespace PaymentGateway\Paddle;
>
> use DateTime;
> use Notification\Email; // IMPORT
>
> class Transaction
> {
> 	public function __construct()
> 	{
> 		var_dump(new Email())
> 	}
> }
> ```

> [!info] How about `Functions`?
> `functions` **when NOT FOUND** in **_LOCAL namespace_**
> **FALLSBACK** into the **_GLOBAL namespace_**
>
> ```php
> declare(strict_types = 1);
>
> namespace PaymentGateway\Paddle;
>
> class Transaction
> {
> 	public function __construct()
> 	{
> 		var_dump(explode(',', 'hello, world'));
> 	}
> }
> ```
>
> ---
>
> if it exists **_locally_**:
> use _backslash_
>
> ```php
> declare(strict_types = 1);
>
> namespace PaymentGateway\Paddle;
>
> class Transaction
> {
> 	public function __construct()
> 	{
> 		var_dump(\explode(',', 'hello, world'));
> 	}
> }
>
> function explode($separator, $str)
> {
> 	return 'foo';
> }
> ```
