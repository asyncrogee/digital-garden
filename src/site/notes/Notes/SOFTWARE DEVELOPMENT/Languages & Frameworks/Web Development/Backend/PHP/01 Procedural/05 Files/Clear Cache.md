---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/05-files/clear-cache/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.330+08:00"}
---


---


#### Clear cache values of `functions` like `filesize`
```php
echo filesize('foo.txt');

file_put_contents('foo.txt', 'hello world');
clearstatcache();

echo filesize('foo.txt');
```

