---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/06-functions/04-named-arguments/","tags":["programming","php","webdevelopment","backend"],"created":"2024-11-09T11:30:30.339+08:00"}
---


--- 
Even the `argument`'s is ___NOT IN ORDER___ the same as the __PARAMETERS__

```php
declare(strict_types=1);

function foo(int $x, int $y): int {
	if ($x % $y === 0) {
		return $x / $y;
	}

	return $x;
}

$x = 6;
$y = 3;

// parameter name: value
echo foo(y: $y, x: $x);

echo foo($x, y: $y);

$arr = ['y' => 1, 'x' => 2];
echo foo(...$arr);
```