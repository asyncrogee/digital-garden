---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/03-operators/05-error-control-operator/","tags":["programming","php","webdevelopment","backend"]}
---


--- 
> [!info] 
> __Supresses Any Error__ from an Expression.
> ```php
> $x = file('foo.txt'); // ERROR: file not found
> 
> $x = @file('foo.txt'); //
> ```
> - NOT Recommended to use
