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

> [!question] Why are `static properties` and `methods` discouraged?
>
> - They represent `Global State`
>   - Because you can **Modify** the `data` or **Call** the `static function` from **Anywhere** in the code
> - Some use-cases are **_MISUSED_** and **DEPENDENCY INJECTION** should be used instead

> [!abstract] >`Static Properties` is like a part of the `Class` itself.
>
> - No need to call the `class` and create a new `object` to access it.
> - Accessed using `::`
>   - `ClassName::$static`
>
> ---
>
> ##### 2 ways to define
>
> ```php
> // 1: Standard
> public static string $variable = 'value';
> //2:
> static public string $variable = 'value';
> ```
>
> ---
>
> _Index.php_
>
> ```php
> use App\PaymentGateway\Paddle\Transaction;
>
> require_one __DIR__ . '/../vendor/autoload.php';
>
> $transaction = new Transaction(25, 'Transaction 1');
>
> //  Don't need to access by `object`
> var_dump($transaction::$count);
>
> // ACCESS DIRECTLY FROM THE CLASS
> var_dump(Transaction::$count);
> ```
>
> _Transaction.php_:
>
> ```php
> declare(strict_types = 1);
>
> namespace App\PaymentGateway\Paddle;
>
> class Transaction
> {
> 	public static int $count =  0;
>
> 	public function __construct(
> 		public float $amount,
> 		public string $description
> 	) {
>
> 	// ACCESS WITHIN the CLASS using `self`
> 		self::$count++;
>
> 	}
>
> 	public function process()
> 	{
> 		echo 'Processing paddle transaction...';
> 	}
> }
> ```
>
> - Access the `static property` using `self` like `self::$count++;`
>
> > [!question] What if the `static property` is **private**?
> > the `static property` would only be **ACCESSIBLE INSIDE THE CLASS**,
> > One way is to create a `public static Method` like this:
> >
> > ```php
> > // ...
> > class Transaction
> > {
> > 	private static int $count = 0;
> >
> > 	// ...
> >
> > 	public static function getCount(): int
> > 	{
> > 		return self::$count;
> > 	}
> > }
> > ```
> >
> > ```php
> > // ...
> >
> > var_dump(Transaction::getCount());
> > ```
