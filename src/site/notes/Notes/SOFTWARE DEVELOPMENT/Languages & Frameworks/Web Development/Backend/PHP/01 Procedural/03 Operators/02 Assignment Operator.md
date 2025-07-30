---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/03-operators/02-assignment-operator/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.266+08:00"}
---


--- 

> [!info] Assignment Operators
>```php
>$x = 5;
>$x = $y = 10;
>var_dump($x, $y); // int(10) int(10)
>
>$x = ($y = 10) + 5;
>var_dump($x, $y); // int(15) int(10)
>
>$x +=  3;
>x *= 3;
>```
