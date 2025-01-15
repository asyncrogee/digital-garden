---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/06-functions/02-parameters-and-arguments/","tags":["programming","php","webdevelopment","backend"],"created":"2024-11-09T11:30:30.329+08:00"}
---


--- 
```php
function foo(int|float $x, int|float $y) {
	return $x * $y;
}

echo foo(5.0, 10); // 50
```

> [!tip] Optional Parameter / Default Value:
> Specifiy the __Default Value__ of a `parameter`
> ```php
> function foo(int|float $x, int|float $y = 10) {
> 	return $x * $y;
> }
> 
> echo foo(5.0); // 50
> ```
> - The __Default Value__ of `$y` will be `10`, __IF NOT SPECIFIED__
>> [!info] Optional Parameter should be after the ___Required parameters___
>> ```php
>> function foo(int|float $x, int|float $y = 10, int|float $z ){
>> 	// THIS WOULD CAUSE AN ERROR
>> 	// The order of parameters above:
>> 	// Required, Optional, Required
>> }
>> ```

> [!info] Modifying a `variable` inside the `function`
> Reference `&`
> ```php
> function foo(int|float &$x, int|float $y): int|float {
> 	if ($x % 2 === 0) {
> 		$x /= 2; // Modifies the first parameter
> 	}
> 	
> 	return $x * $y;
> }
> 
> $a = 6.0;
> $b = 7;
> 
> echo foo($a, $b) . '<br />'; // 21
> 
> // $a got modified and became 3:
> var_dump($a, $b); // float(3) int(7)
> ```
