---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/laravel/01-introduction/03-dynamic-layout/","tags":["programming","Laravel","PHP","layout"],"created":"2025-07-13T15:25:33.838+08:00"}
---

[[02 Layout \|<- Introduction to Laravel Layout]]

For example: Making a Navigation Links dynamic using templates:
```php
	<nav>
		<x-nav-link href="/">Home</x-nav-link>
		<x-nav-link href="/about">About</x-nav-link>
		<x-nav-link href="/contact">Contact</x-nav-link>
	</nav>
```

```php
<a {{ $attributes }}>{{ $slot }}</a>
```
- Remember tho, `$attributes` is an _Object_
	- example: `<a {{ $attributes->merge(['class']) }}>{{ $slot }}</a>`

