---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/02-data-types/06-null/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.224+08:00"}
---



--- 

>[!info] Null Constant
>```PHP
>$x = null;
>$x = NULL;
>
>echo $x; // 
>
>var_dump($x) // NULL
>
>var_dump($x === null); // bool(true)
>
>$y = 123;
>var_dump($y); // int(123)
>unset($y);
>
>var_dump($y); // ERROR and NULL
>
>```
>> [!tip] Check if a variable is `null`
>> ```php
>> is_null($x) //true
>> 
>> var_dump(is_null($x)); // bool(true)
>> ```

> [!TIP] Casting
> ```php
> $x = null;
> 
> var_dump((string) $x); // string(0) ""
> var_dump((int) $x); // int(0)
> var_dump((bool)$x); // bool(false)
> var_dump((array) $x); // array(0) {}
> ```
