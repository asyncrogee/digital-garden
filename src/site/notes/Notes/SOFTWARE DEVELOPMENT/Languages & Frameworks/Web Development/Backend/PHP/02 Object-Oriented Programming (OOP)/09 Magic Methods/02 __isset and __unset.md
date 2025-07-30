---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/09-magic-methods/02-isset-and-unset/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.989+08:00"}
---


---

> [!info] `__isset()`
>
> ```php
> public function __isset(string $name): bool
> {
> 	return array_key_exists($name, $this->data);
> }
> ```
>
> - Its purpose is to determine if the specified property (`$name`) exists within the object and has a value that's not `null`.

> [!info] `__unset()`
>
> ```php
> public function __isset(string $name): void
> {
> 	unset($this->data[$name]);
> }
> ```
