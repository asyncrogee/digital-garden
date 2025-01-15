---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/08-arrays/12-destructure-array/","tags":["programming","php","webdevelopment","backend"],"created":"2024-11-09T11:30:30.572+08:00"}
---


--- 
 >[!info] `list`
 >Assigns the `values` of an __Array__ to `variables`:
 >```php
 >$array = [1, 2, 3, 4];
 >
 >list($a, $b, $c, $d) = $array;
 >
 >// SHORTHAND
 >[$a, $b, $c, $d] = $array; // 1, 2, 3, 4
 >
 >```
 >
 >Skip Elements:
 >```php
 >[$a, , $c, ] =$array; // 1, 3
 >```
 >
 >Nested Arrays:
 >```php
 >$array = [1, 2, [3, 4]];
 >[$a, $b, [$c, $d]] = $array;
 >```
 >
 >Specify `keys`:
 >```php
 >$array = [1, 2, 3];
 >
 >[1 => $a, 0 => $b, 2 => $c] = $array; // 2, 1, 3
 >
 >```



