---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/03-operators/06-increment-decrement-operators/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.255+08:00"}
---


--- 
> [!info]
> ```php
> $x = 5;
> 
> $x++; // Increment
> $x--; // Decrement
> ++$x; // Pre-Increment
> --$x; // Pre-decrement
> ```

```php
$x = 5;

echo $x++; // 5
echo $x; // 6

echo $x--; // 5
echo $x; // 4

echo ++$x; // 6
echo $x; // 6

echo --$x; // 4
echo $x; // 4

```


```php
$x = true;

echo ++$x; // 1

$y = null;
echo ++$y; // 1
echo --$y; // 1

$z = 'abc';
echo ++$z; // 'abd'
```