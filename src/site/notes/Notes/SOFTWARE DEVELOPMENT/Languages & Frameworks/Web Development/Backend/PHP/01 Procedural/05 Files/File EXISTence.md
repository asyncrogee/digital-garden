---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/05-files/file-exis-tence/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.321+08:00"}
---


--- 
#### Check if FILE EXISTS
>[!info] Check if `FILE` __EXISTS__:
>`file_exists('file name')`
>```php
>if (file_exists('foo.txt')) {
>	echo filesize('foo.txt'); // File Size
>} else {
>	echo 'File not found';
>}
>```

