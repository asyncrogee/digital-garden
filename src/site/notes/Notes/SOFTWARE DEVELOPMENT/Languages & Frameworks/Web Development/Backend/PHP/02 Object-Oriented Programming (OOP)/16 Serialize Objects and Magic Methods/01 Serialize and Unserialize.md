---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/16-serialize-objects-and-magic-methods/01-serialize-and-unserialize/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.173+08:00"}
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
> ![[Pasted image 20240330024705.png]]

> [!INFO] `unserialize`
>
> ```php
> var_dump(unserialize(serialize(['a' = 1, 'b' => 2])));
> ```
>
> **_OUTPUT_**:
> ![[Pasted image 20240330024903.png]]
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
> ![[Pasted image 20240330030616.png]]

> [!CAUTION]
> Failed serialization results to `boolean false`
> ![[Pasted image 20240330031139.png]] > **_OUTPUT_**:
> ![[Pasted image 20240330031228.png]]
