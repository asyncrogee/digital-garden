---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/01-classes-and-objects/05-std-class/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:51.557+08:00"}
---


---

```php
$str = '{"a":1, "b":2, "c":3 }';

// 2nd Parameter as TRUE to return it as an ASSOCIATIVE ARRAY
$arr = json_decode($str, true);

var_dump($arr);
```

Output:
![[Pasted image 20240326164843.png]]

**NOT PASSING** the `2nd Parameter`:

```php
$str = '{"a":1, "b":2, "c":3 }';

// 2nd Parameter as TRUE to return it as an ASSOCIATIVE ARRAY
$arr = json_decode($str);

var_dump($arr);
var_dump($arr->a) // OUTPUT: int(1)
```

Output:
![[Pasted image 20240326164957.png]]

> [!tip] Custom `stdClass`
>
> ```php
> $obj = new \stdClass();
>
> $obj->a = 1;
> $obj->b = 2;
>
> var_dump($obj)
> ```
>
> Output:
> ![[Pasted image 20240326165327.png]]
