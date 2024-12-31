---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/08-arrays/11-sort-arrays/","tags":["programming","php","webdevelopment","backend"]}
---


--- 
> [!info] `asort`
> Sort `arrays` by `values`
> ```php
> $array = ['d' => 3, 'b' => 1, 'c' => 4, 'a' => 2];
> 
> asort($array);
> ```


> [!info] `ksort`
> Sort `arrays` by `keys`
> ```php
> ksort($array);
> 
> ```

> [!info] `usort`
> Custom order
> - Accepts a __Callback__ function
> - Removes `Custom Keys`
> Example:
> ```php
> usort($array, fn($a, $b) =>  $a <==> $b); 
> ```
