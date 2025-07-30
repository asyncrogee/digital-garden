---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/12-anonymous-classes/01-anonymous-class/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.070+08:00"}
---


---

> [!info] Anonymous Class
>
> ```php
> $obj = new class(1, 2, 3) {
> 	public function __construct(public int $x, public int $y, public int $z)
> 	{
>
> 	}
> }
> ```
>
> just like a Normal `Class`,
> It can do **Inheritance**, **_Interface_** and _Traits_
>
> ```php
> $obj = new class(1, 2, 3) extends MyClass implements MyInterface
> {
>
> 	Use MyTrait;
>
> 	public function __construct(public int $x, public int $y, public int $z)
> 	{
>
> 	}
> }
> ```

> [!tip] Type Hinting `Anonymous Class`
>
> ```php
> $obj = new class(1, 2, 3) implements MyInterface
> {
> 	public function __construct(public int $x, public int $y, public int $z)
> 	{
> 	}
> };
>
> foo($obj);
>
> function foo(MyInterface $obj)
> {
> 	var_dump($obj)
> }
> ```

> [!tip] Nesting `Anonymous Classes`
>
> ```php
> namespace App;
>
> class ClassA
> {
> 	public function __construct(public int $x, public int $y)
> 	{
> 	}
>
> 	public function foo(): string
> 	{
> 		return 'foo';
> 	}
>
> 	public function bar(): object
> 	{
> 		return new class {
>
> 		}
> 	}
> }
> ```
>
> ```php
> $obj = new ClassA(1, 2);
>
> var_dump($obj->bar());
> ```
>
> - `Properties` and `Methods` of the **MAIN CLASS** (`ClassA`) **_CANNOT BE ACCESSED_** by the _ANONYMOUS CLASS_ inside `bar()`
>
> ```php
> public function bar(): object
> {
> 	return new class {
> 		echo $this->y;
> 	}
> }
> ```
