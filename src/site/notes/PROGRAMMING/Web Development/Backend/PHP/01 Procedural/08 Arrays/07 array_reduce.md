---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/08-arrays/07-array-reduce/","tags":["programming","php","webdevelopment","backend"]}
---


--- 
> [!info]
> Reduce the `array` to a Single Value
> `array_reduce($array, callback function)`
> ```php
> array_reduce($array, fn() => ;)
> ```
> 
> ![Pasted image 20240316142218.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/01%20Procedural/08%20Arrays/attachments/Pasted%20image%2020240316142218.png)
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

