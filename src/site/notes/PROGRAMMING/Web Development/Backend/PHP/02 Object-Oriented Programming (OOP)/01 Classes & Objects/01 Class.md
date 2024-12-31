---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/02-object-oriented-programming-oop/01-classes-and-objects/01-class/","tags":["programming","php","webdevelopment","backend","OOP"]}
---


---

> [!info] `Class`
>
> - Class **Name** could begin with `Letters` or `Underscores` (`_`)
> - Recommended is `1` Single **Class** per File and nothing else in that File.
>   > [!example]
>   >
>   > > [!note] _Transaction.php_
>   > >
>   > > ```php
>   > > // Defining a CLASS
>   > > class Transaction
>   > > {
>   > > 	public $amount;
>   > > 	public $description;
>   > > }
>   > > ```
>   >
>   > - `public` means it's available to those interacting with the `object` **even outside of the `class`**
>   >   - `public` properties _values_ can be changed.
>   > - `properties` with No Value, are automatically set to `NULL`
>   >
>   > > [!note] _In another file_:
>   > >
>   > > ```php
>   > > require_once '../Transaction.php';
>   > >
>   > > $transaction = new Transaction();
>   > >
>   > > $transaction -> amount  = 15;
>   > >
>   > > var_dump($transaction -> amount); // int(15)
>   > > ```
>   >
>   > - `->` **Object operator**
>   >
>   > > [!caution] Defining Property Types
>   > > `Property` should **_NOT be accessed_** before _Initialization_
>   > >
>   > > ```php
>   > > declare(strict_types=1);
>   > >
>   > > class Transaction
>   > > {
>   > > 	public float $amount;
>   > > 	public string $description;
>   > > 	public $prop;
>   > > }
>   > >
>   > > // In another file:
>   > > var_dump($transaction->amount); // FATAL ERROR!
>   > >
>   > > var_dump($transaction); // "amount" => uninitialized(float) "description"=>uninitialized(string)
>   > > var_dump($transaction); // (same as above, then) "prop"=> NULL
>   > > ```
