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

```php
$str = '{"a":1, "b":2, "c":3 }';

// 2nd Parameter as TRUE to return it as an ASSOCIATIVE ARRAY
$arr = json_decode($str, true);

var_dump($arr);
```

Output:
![Pasted image 20240326164843.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/01%20Classes%20&%20Objects/attachments/Pasted%20image%2020240326164843.png)

**NOT PASSING** the `2nd Parameter`:

```php
$str = '{"a":1, "b":2, "c":3 }';

// 2nd Parameter as TRUE to return it as an ASSOCIATIVE ARRAY
$arr = json_decode($str);

var_dump($arr);
var_dump($arr->a) // OUTPUT: int(1)
```

Output:
![Pasted image 20240326164957.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/01%20Classes%20&%20Objects/attachments/Pasted%20image%2020240326164957.png)

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
> ![Pasted image 20240326165327.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/01%20Classes%20&%20Objects/attachments/Pasted%20image%2020240326165327.png)
