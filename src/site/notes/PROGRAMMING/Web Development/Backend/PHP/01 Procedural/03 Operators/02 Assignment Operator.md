---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/03-operators/02-assignment-operator/","tags":["programming","php","webdevelopment","backend"],"created":"2024-11-09T11:30:30.056+08:00"}
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
