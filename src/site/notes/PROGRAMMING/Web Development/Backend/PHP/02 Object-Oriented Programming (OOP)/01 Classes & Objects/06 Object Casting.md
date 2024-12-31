---
ProgrammingLanguage: PHP
tags:
  - programming
  - php
  - webdevelopment
  - backend
  - OOP
dg-publish: true
Topic: OOP
---

---

Convert `array` to `object`:

```php
$arr = [1, 2, 3];

var_dump((object) $arr);
```

Output:
![Pasted image 20240326165601.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/01%20Classes%20&%20Objects/attachments/Pasted%20image%2020240326165601.png)

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
