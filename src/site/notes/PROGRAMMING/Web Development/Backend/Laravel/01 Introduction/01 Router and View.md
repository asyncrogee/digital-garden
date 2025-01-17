---
{"dg-publish":true,"permalink":"/programming/web-development/backend/laravel/01-introduction/01-router-and-view/","tags":["programming","Laravel","PHP","route"],"created":"2025-01-17T13:19:35.717+08:00"}
---

```php
<?php

use Illuminate\Support\Facades\Route;

Route::get('/', function () {
    return view('home');
});

Route::get('/about', function(){
    return view('about');
});

Route::get('/contact', function() {
    return view('contact');
});
```

- We're declaring a `Route` that listens to a `get()` request
- Listens to the URL (the __first parameter__ of `get()` function), then triggers the ___second parameter___ / function

```php
Route::get('/', function () {
    return view('home');
});
```
- `view()` function reads from the __views folder__ inside _resources folder_
	- here it returns the `home` file (could either be `home.blade.php` or `home.php`)


---
### Other ways to use it:
###### Returning a String
```php
Route::get('/about', function () {
    return 'About Page';
});
```

###### Returning an Array:
- Can be useful for building an API
```php
Route::get('/about', function () {
    return ['foo' => 'bar'];
});
```


