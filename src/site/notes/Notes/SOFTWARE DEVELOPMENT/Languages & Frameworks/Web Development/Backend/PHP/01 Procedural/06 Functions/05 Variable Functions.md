---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/06-functions/05-variable-functions/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.362+08:00"}
---


--- 

```php
function sum(int|float ...$numbers): int|float {
	return array_sum($numbers);
}

$x = 'sum';

echo $x(1, 2, 3, 4);
```

Prevent an error, if not sure the `variable` is a __callable `function`__
```php
function sum(int|float ...$numbers): int|float {
	return array_sum($numbers);
}

$x = 'sum';

if (is_callable($x)) {
	echo $x(1, 2, 3, 4);
} else {
	echo 'Not Callable';
}

```