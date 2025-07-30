---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/01-classes-and-objects/06-object-casting/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:51.547+08:00"}
---


---

Convert `array` to `object`:

```php
$arr = [1, 2, 3];

var_dump((object) $arr);
```

Output:
![[Pasted image 20240326165601.png]]

#### Accessing properties

```php
$arr = [1, 2, 3];
$obj = (object) $arr;

var_dump($obj->{1}); // OUTPUT: int(2)
```

> [!tip] scalar property
>
> - **Integer** to `object`
>
> ```php
> $obj = (object) 1;
>
> var_dump($obj->scalar); // int(1)
> ```
>
> - **Boolean** to `object`
>
> ```php
> $obj = (object) true;
>
> var_dump($obj->scalar); // bool(true)
> ```

> [!info] NULL to object
> Converting **NULL** to an `object` will result to an **_EMPTY OBJECT_**
>
> ```php
> $obj = (object) null;
> var_dump($obj);
> ```
