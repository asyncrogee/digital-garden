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
> The `serialize()` function in PHP is used to convert a PHP value into a storable representation, which is a `string`.
> This `string` representation can then be saved to a **file**, a **database**, or **transmitted across a network**.

> [!info] `serialize`
>
> ```php
> echo serialize(true) . PHP_EOL;
> echo serialize(1) . PHP_EOL;echo serialize(true) . PHP_EOL;
> echo serialize(2.5) . PHP_EOL;
> echo serialize('hello world') . PHP_EOL;
> echo serialize([1, 2, 3]) . PHP_EOL;
> echo serialize(['a' => 1, 'b' => 2]) . PHP_EOL;
> ```
>
> **_OUTPUT_**:
> ![Pasted image 20240330024705.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/16%20Serialize%20Objects%20and%20Magic%20Methods/attachments/Pasted%20image%2020240330024705.png)

> [!INFO] `unserialize`
>
> ```php
> var_dump(unserialize(serialize(['a' = 1, 'b' => 2])));
> ```
>
> **_OUTPUT_**:
> ![Pasted image 20240330024903.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/16%20Serialize%20Objects%20and%20Magic%20Methods/attachments/Pasted%20image%2020240330024903.png)
>
> - `unserialize`-ing **CREATES A NEW** `OBJECT`
>
> ```PHP
> $invoice = new Invoice();
>
> $str = serialize($invoice);
>
> $invoice2 = unserialize(str);
>
> var_dump($invoice, $invoice2, $invoice === $invoice2);
> ```
>
> **_OUTPUT_**:
> ![Pasted image 20240330030616.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/16%20Serialize%20Objects%20and%20Magic%20Methods/attachments/Pasted%20image%2020240330030616.png)

> [!CAUTION]
> Failed serialization results to `boolean false`
> ![Pasted image 20240330031139.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/16%20Serialize%20Objects%20and%20Magic%20Methods/attachments/Pasted%20image%2020240330031139.png) > **_OUTPUT_**:
> ![Pasted image 20240330031228.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/16%20Serialize%20Objects%20and%20Magic%20Methods/attachments/Pasted%20image%2020240330031228.png)
