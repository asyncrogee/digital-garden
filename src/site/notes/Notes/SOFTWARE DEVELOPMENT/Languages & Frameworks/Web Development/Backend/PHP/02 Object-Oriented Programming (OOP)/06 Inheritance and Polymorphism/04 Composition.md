---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/06-inheritance-and-polymorphism/04-composition/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.905+08:00"}
---


---

#### Composition

![[Pasted image 20240328133233.png]]

> [!info] COMPOSITION
> Instead of **_EXTENDing_** `ToasterPro`,
> We can use a **COMPOSITION**:
>
> So that _FancyOver_ will have `ToasterPro`'s **Functionality**.
>
> _FancyOven.php_
>
> ```php
> namespace App;
>
> class FancyOver
> {
>
> // COMPOSITION
> 	private ToasterPro $toaster;
>
> 	public function fry(ToasterPro $toaster)
> 	{
> 		$this ->toaster = $toaster;
> 	}
>
> 	// OR with Property Promotion:
> 	public function __construct(private ToasterPro $toaster)
> 	{
> 	}
>
> 	public function fry()
> 	{
> 		// fry stuff
> 	}
>
>
> 	public function toast()
> 	{
> 		$this->toaster->toast();
> 	}
>
> 	public function toastBagel()
> 	{
> 		$this->toaster->toastBagel();
> 	}
> }
> ```
