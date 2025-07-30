---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/05-encapsulation-and-abstraction/01-encapsulation/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.882+08:00"}
---


---

> [!abstract] Encapsulation
>
> - Bundles `data`
>   - and `methods` that **operate in that** `data`
> - Makes sure that `object` **manages it's own state** - `properties` shouldn't be modified outside the class. -
>   > [!caution] Example:
>   >
>   > ```php
>   > // ...
>   > $transaction = new Transaction(25);
>   > $transaction->process(); // Processing $25 transaction
>   >
>   > // MODIFYING IT:
>   > $transaction->amount = 125;
>   >
>   > $transaction->process(); // Processing $125 transaction
>   >
>   > ```
>   >
>   > ***
>   >
>   > ##### Getter and Setter Methods
>   >
>   > ```php
>   > class Transaction
>   > {
>   > 	private float $amount;
>   >
>   > 	public function __construct()
>   > 	{
>   > 	}
>   >
>   > 	// prints the Amount
>   > 	public function getAmount(): float
>   > 	{
>   > 		return $this->amount;
>   > 	}
>   >
>   > 	// Modifies the Amount
>   > 	public function setAmount(float $amount): float
>   > 	{
>   > 		$this->amount = $amount;
>   > 	}
>   >
>   > 	public function process()
>   > 	{
>   > 		echo 'Processing 
 . $this->amount . ' transaction';
>   > 	}
>   > }
>   > ```
