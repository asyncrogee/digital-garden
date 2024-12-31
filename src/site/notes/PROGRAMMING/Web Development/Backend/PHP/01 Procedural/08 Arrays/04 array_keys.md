---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/08-arrays/04-array-keys/","tags":["programming","php","webdevelopment","backend"]}
---


--- 
> [!info] Syntax:
> Get `keys` of an Array
> - First argument, the array
> - Second, to find the specific `key` from a __value__.
> - Third, (`true/false`) whether to Turn __Strict Mode__ ON
> ```php
> $array = ['a' => 5, 'b' => 10. 'c' => 15, 'd' => 5, 'e' => 10];
> 
> $keys = array_keys($array, 15); // c
> 
> // with STRICT MODE turned ON
> $keys = array_keys($array, '15', true); // empty / none
> ```
