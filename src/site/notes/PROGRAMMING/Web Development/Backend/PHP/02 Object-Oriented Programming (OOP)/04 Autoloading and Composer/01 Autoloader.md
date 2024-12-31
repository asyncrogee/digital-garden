---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/02-object-oriented-programming-oop/04-autoloading-and-composer/01-autoloader/","tags":["programming","php","webdevelopment","backend","OOP"]}
---


---

> [!INFO]
>
> - Helps in Code readability,
>   - Doesn't need to put `include` or `requires`
> - Automatically loads `classes`, `interfaces` or `traits` that are **_not included or defined_**

```php
spl_autoload_register(function($class) {
	var_dump('Autoloader 1:');
});

spl_autoload_register(function($class) {
	var_dump('Autoloader 2:');
}, prepend: true); // Prepend set to TRUE, means this would run FIRST


use App\PaymentGateway\Paddle\Transaction;

$paddleTransaction = new Transaction();

var_dump($paddleTransaction);
```

> [!example] `require` a path inside `autoloader`
>
> ```php
> spl_autoload_register(function($class) {
>
> 	$path = __DIR__ . '/../' . lcfirst(str_replace('\\', '/', $class)) . '.php';
>
> 	require $path;
> });
>
> use App\PaymentGateway\Paddle\Transaction;
>
> $paddleTransaction = new Transaction();
>
> var_dump($paddleTransaction);
> ```
>
> - `__DIR__` is a **Magic Function**
> - `lcfirst()` - Lower Cases the First Letter
> - `str_replace()` - Replaces _backslash_ with **Normal Slash**
