---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/01-procedural/05-files/directories/","tags":["programming","php","webdevelopment","backend"],"created":"2025-07-13T15:24:51.327+08:00"}
---


--- 

> [!info] `scandir()`
> ```php
> $dir = scandir(__DIR__);
> 
> var_dump($dir);
> var_dump($dir[2]); // string "index.php"
> ```
> - `__DIR__` = __Current Directory__
> Output:
> ![[Pasted image 20240317113014.png]]
> - Index `0` (`.`) is the __Current Directory__
> - Index `1` (`..`) is the ___Parent Directory___
> - Index `2` (`index.php`) which is the only file in the Directory.
> - 
>
>> [!tip] Check if a __File__ or a ___Directory___
>> ```php
>>  var_dump(is_file($dir[2])); // bool(true)
>>  
>>  var_dump(is_dir($dir[2])); // bool(false)
>> ```

#### Create Directory
```php
mkdir('directory name');
```

##### Recursive Directory
```php
mkdir('foo/bar', recursive: true);

rmdir('foo/bar'); // Deletes Directory "bar"
rmdir('foo');
```

#### Delete Directory
```php
rmdir('directory name');
```
- ___Directory___ should be __EMPTY__ before deleting
	- Otherwise, ___WARNING___!