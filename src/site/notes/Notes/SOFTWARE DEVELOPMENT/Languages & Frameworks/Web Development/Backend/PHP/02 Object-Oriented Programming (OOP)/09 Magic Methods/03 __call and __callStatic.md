---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/09-magic-methods/03-call-and-call-static/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.984+08:00"}
---


---

> [!info] `__call`
>
> - Called when an **Inaccessible `Method`** is **CALLED**
>
> ```php
> public function __call(string $name, array $arguments)
> {
> 	var_dump($name, $arguments);
> }
> ```
>
> - In this case, we `var_dump` the `Method`'s name and it's `Properties`
>
> > [!example]
> > What if the `METHOD` **accepts some `arguments`?**
> >
> > ```php
> > class Invoice
> > {
> > 	protected function process()
> > 	{
> > 		var_dump($amount, $description);
> > 	}
> >
> > 	public function __call(string $name, array $arguments)
> > 	{
> > 		if (method_exists($this, $name))
> > 		{
> > 		// INSTEAD OF:
> > 		// $this->$name($arguments);
> > 			call_user_func_array([$this, $name], $arguments);
> > 		}
> > 	}
> > }
> > ```

> [!info] `__callStatic`
>
> - Called when an **Inaccessible STATIC `Method`** is **CALLED**
>
> ```php
> public static function __callStatic(string $name, array $arguments)
> {
> 	var_dump('static', $name, $arguments);
> }
> ```
