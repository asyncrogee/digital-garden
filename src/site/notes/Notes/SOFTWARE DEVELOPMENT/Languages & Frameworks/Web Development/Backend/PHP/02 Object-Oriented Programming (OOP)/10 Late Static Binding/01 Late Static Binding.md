---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/10-late-static-binding/01-late-static-binding/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:55.001+08:00"}
---


---

https://www.youtube.com/watch?v=4W5t8g3Rp_0&list=PLr3d3QYzkw2xabQRUpcZ_IBk9W50M9pe-&index=48&ab_channel=ProgramWithGio

> [!abstract]
>
> ##### 2 Types of Binding
>
> - **EARLY BINDING**
>   - Compile Time
>     - `Static Properties`
>     - `Static Methods`
> - **LATE BINDING**
>   - Runtime
>     - `Late Static Binding`

> [!example] >_ClassA.php_
>
> ```php
> namespace App;
>
> class ClassA
> {
> 	protected string $name = 'A';
>
> 	public function getName(): string
> 	{
> 		return $this->name;
> 	}
> }
> ```
>
> _ClassB.php_
>
> ```php
> namespace App;
>
> class ClassB extends ClassA
> {
> 	protected string $name = 'B';
> }
> ```
>
> _Index.php_
>
> ```php
> require_once __DIR__ . '/.../vendor/autoload.php';
>
> $classA = new \App\ClassA();
> $classB = new \App\ClassB();
>
> echo $classA->getName() . PHP_EOL;
> echo $classB->getName() . PHP_EOL;
> ```
>
> **_OUTPUT_**:
>
> ```
> A
> B
> ```

---

#### Problem:

_ClassA.php_

```php
namespace App;

class ClassA
{
	protected static string $name = 'A';

	public static function getName(): string
	{
		var_dump(self::class);
		return self::name;
	}
}
```

_ClassB.php_

```php
namespace App;

class ClassB
{
	protected static string $name = 'B';
}
```

_index.php_

```php
require_once __DIR__ . '/../vendor/autoload.php';

echo \App\ClassA::getName() . PHP_EOL;
echo \App\ClassB::getName() . PHP_EOL;
```

**_OUTPUT_**:

```
string(10) "App\ClassA"
A
string(10) "App\ClassA"
A
```

- Every time `return self::name;` it still refers to `Class A`
  - `self` doesn't follow the same **_inheritance rules_**

---

### Solution: `static` keyword

_ClassA.php_

```php
namespace App;

class ClassA
{
	protected static string $name = 'A';

	public static function getName(): string
	{
		return static::name;
	}
}
```

_index.php_

```php
require_once __DIR__ . '/../vendor/autoload.php';

echo \App\ClassA::getName() . PHP_EOL;
echo \App\ClassB::getName() . PHP_EOL;
```

- When `static` keyword is encountered,
  - It refers **Directly to the left of the `::`\_**
    - `\App\ClassB`

Another example:

```php
public static function make(): static
{
	return new static();
}
```

```php
var_dump(\App\ClassB::make());
```
