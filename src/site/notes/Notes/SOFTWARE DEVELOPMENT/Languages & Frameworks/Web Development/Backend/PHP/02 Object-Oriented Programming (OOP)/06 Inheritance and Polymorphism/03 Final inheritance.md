---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/06-inheritance-and-polymorphism/03-final-inheritance/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.912+08:00"}
---


---

#### Final `Class`/`Method`

> [!INFO] FINAL `class` and `method`
> Define `Class`/`Method` as **FINAL**
>
> - CANNOT BE INHERETED OR EXTENDED
>
> ```php
> final class Toaster {
> 	// ...
> }
>
> // IN ANOTHER FILE:
> class ToasterPro extends Toaster
> {
> 	// THIS WOULD RESULT TO A FATAL ERROR!
> }
>
> ```
