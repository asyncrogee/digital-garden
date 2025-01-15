---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/08-arrays/08-array-search/","tags":["programming","php","webdevelopment","backend"],"created":"2024-11-09T11:30:30.527+08:00"}
---


--- 
 >[!info]
 >Finding the `key` of a certain `value`
 >- Is __Case-Sensitive__
 >```php
 >$array = ['a', 'b', 'c', 'D', 'E', 'ab', 'bc', 'cd', 'b', 'd'];
 >
 >$key = array_search('b', $array); // int(1)
 >```