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

#### Composition

![Pasted image 20240328133233.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/06%20Inheritance%20and%20Polymorphism/attachments/Pasted%20image%2020240328133233.png)

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
