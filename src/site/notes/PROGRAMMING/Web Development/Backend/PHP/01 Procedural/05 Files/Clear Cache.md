---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/05-files/clear-cache/","tags":["programming","php","webdevelopment","backend"],"created":"2024-11-09T11:30:30.682+08:00"}
---


---


#### Clear cache values of `functions` like `filesize`
```php
echo filesize('foo.txt');

file_put_contents('foo.txt', 'hello world');
clearstatcache();

echo filesize('foo.txt');
```

