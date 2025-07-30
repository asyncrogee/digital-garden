---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/06-functions/08-arrow-function/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.350+08:00"}
---

--- 
Normal Function:
```php
$array2 = array_map(function($number) {
	return $number * $number;
}, $array);
```

> [!info] Arrow Function Version:
> ```php
> $array2 = array_map(fn($number) => $number * number, $array);
> ```
> We can use `variables` in the __Parent/Local Scope__ without the need for `use()`:
> BUT __CANNOT BE MODIFIED__
> ```php
> $y = 5;
> $array2 = array_map(fn($number) => $number * number * ++$y, $array);
> 
> echo $y; // 5
> ```
