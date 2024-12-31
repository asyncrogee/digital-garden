---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/08-arrays/01-array-chunk/","tags":["programming","php","webdevelopment","backend"]}
---


--- 
Split the `array` in __Chunks__:
> [!info] Syntax
> - First argument, the `variable`
> - Second, the __number__ of `chunks`
> - Third (___Is OPTIONAL___), Either to __Preserve__ the `Keys` or not.
> ```php
> array_chunk($variable, 2, true);
> ```

Example: 
```php
$items = ['a' => 1, 'b' => 2, 'c' => 3, 'd' => 4, 'e' => 5];

array_chunk($items, 2); // Doesn't Preserve Keys
array_chunk($items, 2, true); // Preserve Keys
```
- __Preserved Keys__:
![Pasted image 20240316101917.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/01%20Procedural/08%20Arrays/attachments/Pasted%20image%2020240316101917.png)
- ___Not Preserved___:
![Pasted image 20240316101901.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/01%20Procedural/08%20Arrays/attachments/Pasted%20image%2020240316101901.png)