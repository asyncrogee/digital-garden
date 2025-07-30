---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/08-arrays/01-array-chunk/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.449+08:00"}
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
![[Pasted image 20240316101917.png]]
- ___Not Preserved___:
![[Pasted image 20240316101901.png]]