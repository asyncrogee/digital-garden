---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/01-classes-and-objects/03-method-chaining/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:51.554+08:00"}
---


---

> [!INFO] Method Chaining
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
> 	public function addTax(float $rate): Transaction
> 	{
> 		$this->amount += $this->amount * $rate / 100;
>
> 		return $this;
> 	}
>
> 	public function applyDiscount(float $rate): Transaction
> 	{
> 		$this->amount -= $this->amount * $rate / 100;
>
> 		return $this;
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
> // Different ways you can do with Method Chaining:
> $transaction = new Transaction(100, 'Transaction 1');
> $transaction->addTax(8)->applyDicount(10);
> //
> $transaction = (new Transaction(100, 'Transaction 1'))->addTax(8)->applyDicount(10);
> //
> $transaction = (new Transaction(100, 'Transaction 1'))
> 	->addTax(8)
> 	->applyDicount(10);
>
> 	//
> $amount = (new Transaction(100, 'Transaction 1'))
> 	->addTax(8)
> 	->applyDiscount(10)
> 	->getAmount();
>
> var_dump($amount);
> ```
