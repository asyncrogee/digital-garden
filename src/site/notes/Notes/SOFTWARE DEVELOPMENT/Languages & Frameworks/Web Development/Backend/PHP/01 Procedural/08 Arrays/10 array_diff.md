---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/08-arrays/10-array-diff/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.416+08:00"}
---


--- 
> [!info] `array_diff`
>  Checks `values` that are __NOT Present__ in other `arrays`
>  - __ONLY CHECKS `VALUES`__ Not the `keys`
>  ![[Pasted image 20240316144135.png]]
>  ```php
> print_r(array_diff($array1, $array2, $array3)); // [a] => 1, [b] => 2
>  ```
>  - Checks `values` from the __First Argument/Array__ that are not present in the ___REST OF OTHER ARRAYS___.
>> [!tip] `array_diff_assoc`
>> - Also __CHECKS THE `keys`__ with `value` pair.
>>
>> ```php
>> print_r(array_diff_assoc($array1, $array2, $array3)); // [a] => 1, [b] => 2, [c] => 3, [d] => 4, [e] => 5
>> ```
>> 
>
>> [!tip] `array_diff_key`
>>Checks only the `keys`
>>```php
>>array_diff_key($array1, $array2, $array3); // a, b, c, e
>>```


