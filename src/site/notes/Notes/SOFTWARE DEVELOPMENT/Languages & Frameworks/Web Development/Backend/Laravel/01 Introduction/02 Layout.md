---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/laravel/01-introduction/02-layout/","tags":["programming","Laravel","PHP","layout"],"created":"2025-07-13T15:25:33.841+08:00"}
---


> [!abstract] Why?
> - Prevents re-writing of code
> 	- For example:
> 		- Headers
> 		- Navbars

##### Steps:
- Create a folder inside `resources/views` and name it `Components`
	- It will look like this: `*/resources/views/Components`
- Create a _*.blade.php_ file, e.g. `layout.blade.php`
Inside `layout.blade.php`:
```php
<!DOCTYPE html>
<html lang="{{ str_replace('_', '-', app()->getLocale()) }}">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />

        <title>Laravel</title>
    </head>
    <body class="font-sans antialiased dark:bg-black dark:text-white/50">
        <nav>
            <a href="/">Home</a>
            <a href="/about">About</a>
            <a href="/contact">Contact</a>
        </nav>

        <!-- <?php echo $slot ?> -->
        {{ $slot }}
    </body>
</html>
```

##### Using the Layout / Template:
We use it like a __Custom HTML element or tag__ `<x-layout></x-layout>`

For example, using that inside _about.blade.php_ / About Page:
```php
<x-layout>
    <h1>About page</h1>
</x-layout>
```
- We slot the other content of the page inside `<x-layout>` tags,
	- `<h1>` is slotted inside
- Inside, the `layout.blade.php`, we put `$slot` to know where the slotted code will go.

Long Form:
```php
	<?php echo $slot ?>
```
Short Form:
```php
	{{ $slot }}
```

---

[[03 Dynamic Layout \|Dynamic Layout ->]]

