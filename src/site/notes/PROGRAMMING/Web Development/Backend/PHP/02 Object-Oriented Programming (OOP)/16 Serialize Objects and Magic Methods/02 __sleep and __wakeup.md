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
> ![Pasted image 20240330032207.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/16%20Serialize%20Objects%20and%20Magic%20Methods/attachments/Pasted%20image%2020240330032207.png)
>
> - `__sleep` must return the **names** of the `properties` that should be `serialized`
