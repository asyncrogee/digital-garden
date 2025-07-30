---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/08-arrays/07-array-reduce/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.429+08:00"}
---


--- 
> [!info]
> Reduce the `array` to a Single Value
> `array_reduce($array, callback function)`
> ```php
> array_reduce($array, fn() => ;)
> ```
> 
> ![[Pasted image 20240316142218.png]]
> ```php
> $total = array_ reduce ($invoiceItems, fn($sum, $item) => $sum + $item['qty'] * $item['price']); // 258.9
> ```
> - `$sum` is the __Previous__ value
> 	- Initially, `$sum` is zero (`0`) or `null` 
> - `$item` is the current value
> To set the __Initial Value__:
> ```php
> $total = array_ reduce (
> 	$invoiceItems, 
> 	fn($sum, $item) => $sum + $item['qty'] * $item['price'],
> 	500
> 	); // 758.9
> ```

