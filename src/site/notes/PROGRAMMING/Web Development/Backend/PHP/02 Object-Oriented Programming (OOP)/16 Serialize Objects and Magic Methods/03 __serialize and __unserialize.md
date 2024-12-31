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

> [!abstract]
> A combination of `__sleep`, `__wakeup` & `\Serializable` Interface
>
> - When `__serialize` or `__unserialize` is **present** together with `__sleep` or `__wakeup`
>   - `__sleep` and `__wakeup` **will get ignored**

> [!info] `__serialize()`
>
> ```php
> public function __serialize(): array
> {
> 	return [
> 		'id' => $this->id,
> 		'amount' => $this->amount,
> 		'description' => $this->description,
> 		'creditCardNumber' => base64_ encode($this->creditCardNumber),
> 		'foo' => 'bar',
> 	]
> }
> ```
>
> **_OUTPUT_**:
> ![Pasted image 20240330032807.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/16%20Serialize%20Objects%20and%20Magic%20Methods/attachments/Pasted%20image%2020240330032807.png)
>
> - `__serialize()` must return an **array that represents the `object`**

> [!info] `__unserialize()`
> Gets the `data` that was **Unserialized** as the **ARGUMENT**
>
> ```PHP
> public function __unserialize(array $data): void
> {
> 	var_dump($data);
> }
> ```
>
> ```php
> $str = serialize($invoice);
>
> $invoice2 = unserialize($str);
> ```
>
> **_OUTPUT_**:
> ![Pasted image 20240330033345.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/16%20Serialize%20Objects%20and%20Magic%20Methods/attachments/Pasted%20image%2020240330033345.png)
>
> ---
>
> ![Pasted image 20240330033501.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/16%20Serialize%20Objects%20and%20Magic%20Methods/attachments/Pasted%20image%2020240330033501.png)
> ![Pasted image 20240330033530.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/16%20Serialize%20Objects%20and%20Magic%20Methods/attachments/Pasted%20image%2020240330033530.png)
