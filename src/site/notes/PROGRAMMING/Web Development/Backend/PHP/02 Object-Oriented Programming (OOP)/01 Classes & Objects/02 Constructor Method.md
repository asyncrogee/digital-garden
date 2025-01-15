---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/02-object-oriented-programming-oop/01-classes-and-objects/02-constructor-method/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2024-11-09T11:30:31.408+08:00"}
---


---

> [!INFO] Constructor Method
> A special function / **_Magic Method_**
>
> - Called when a **new instance** of the `class` is created.
>
> ```php
> class Transaction
> {
> 	// Setting the amount to private because it shouldn't be change-able
> 	private float $amount;
> 	private string $description;
>
>
> 	public function __construct(float $amount, string $description)
> 	{
> 		$this->amount = $amount;
> 		$this->description = $description
> 	}
>
> 	public function addTax(float $rate)
> 	{
> 		$this->amount += $this->amount * $rate / 100;
> 	}
>
> 	public function applyDiscount(float $rate)
> 	{
> 		$this->amount -= $this->amount * $rate / 100;
> 	}
>
> 	// To atleast view the amount:
> 	public function getAmount(): float
> 	{
> 		return this->$amount;
> 	}
> }
> ```
>
> _In another file:_
>
> ```php
> declare(strict_types=1);
>
> require_once '../Transaction.php';
>
> // Classes & Objects
> $transaction = new Transaction(100, 'Transaction 1');
>
> $transaction->addTax(8); // 108
> $transaction->applyDicount(10); // 97.2
>
> ```
