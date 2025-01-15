---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/08-arrays/06-array-merge/","tags":["programming","php","webdevelopment","backend"],"created":"2024-11-09T11:30:30.500+08:00"}
---


--- 
> [!info] 
> Merge multiple arrays
> - If `arrays` have __THE SAME NUMBERIC `keys`__ 
> 	- they will be __APPENDED__
> - `keys` will be __RE-ORDERED__
> ```php 
> $array1 = [1, 2, 3];
>  $array2 = [6 => 4, 7 => 5, 8 => 6];
>   $array1 = [7, 8, 9];
>   
>$merged = array_merge($array1, $array2, $array3); // 1, 2, 3, 4, 5, 6, 7, 8, 9
> ```
> 
>> [!tip] Overwriting
>> ```php
>> $array1 = [1, 2, 3];
>>  $array2 = ['a' => 4, 'b' => 5, 'c' => 6];
>>   $array1 = [7, 8, 9, 'b' => 10];
>>   
>>   $merged = array_merge($array1, $array2, $array3); // 1, 2, 3, [a] => 4, [b] => 10, [c] => 7, 8, 9
>> ```

