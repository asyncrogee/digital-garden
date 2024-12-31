---
ProgrammingLanguage: PHP
tags:
  - programming
  - php
  - webdevelopment
  - backend
  - OOP
dg-publish: true
Topic: OOP
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
