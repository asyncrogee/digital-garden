---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/08-arrays/05-array-map/","tags":["programming","php","webdevelopment","backend"],"created":"2024-11-09T11:30:30.509+08:00"}
---


--- 
> [!info] 
> Applies `callback` to __each element__ of the given `array`.
> 
> Example: Multiplies each element to 3
> ```php
> $array = [1, 2, 3, 4, 5, 6];
> $array = array_map(fn($number) => $number * 3, $array);
> ```
> Multiple Arrays:
> - `values` will be re-Indexed
> 	- Not preserving it's `keys`
> ```php
> $array1 = ['a' => 1, 'b' => 2, 'c' => 3];
> $array2 = ['d' => 4, 'e' => 5, 'f' => 6];
> 
> $array = array_map(fn($number1, $number2) => $number1 * $number2, $array1, $array2);
> ```

