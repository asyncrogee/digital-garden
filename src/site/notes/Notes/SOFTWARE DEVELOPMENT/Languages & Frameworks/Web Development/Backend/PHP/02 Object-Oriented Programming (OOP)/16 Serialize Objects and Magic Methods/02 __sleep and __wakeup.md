---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/16-serialize-objects-and-magic-methods/02-sleep-and-wakeup/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.169+08:00"}
---


---

> [!abstract] difference
>
> - `__sleep()` - called **before the `serialization` happens**
> - `__wakeup()` - called **_after the `serialization` happens_**

> [!info]
>
> ```php
> class Invoice
> {
> 	public string $id;
>
> 	public function __construct (
> 		public float $amount,
> 		public string $description,
> 		public string $creditCardNumber
> 	) {
> 		$this->id = uniqid('invoice_');
> 	}
>
> 	public function __sleep(): array
> 	{
> 		return['id', 'amount'];
> 	}
>
> 	public function __wakeup(): void
> 	{
> 		// TODO: Implement __wakeup() method.
> 	}
> }
> public function __sleep(): array
> {
> 	return ['id', 'amount'];
> }
> ```
>
> ![[Pasted image 20240330032207.png]]
>
> - `__sleep` must return the **names** of the `properties` that should be `serialized`
