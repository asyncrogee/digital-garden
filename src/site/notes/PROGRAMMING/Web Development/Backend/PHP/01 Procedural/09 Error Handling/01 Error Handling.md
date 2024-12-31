---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/09-error-handling/01-error-handling/","tags":["programming","php","webdevelopment","backend"]}
---


--- 
https://www.php.net/manual/en/errorfunc.constants.php

```php
error_reporting(0); // Turn off reporting errors
error_reporting(E_ALL); // Enable all error reporting including warnings

error_reporting(E_ALL & ~E_WARNING);
```


>[!TIP] `trigger_error`
>User Error Constants
>```php
>trigger_error('Example error', E_USER_ERROR);
>```
