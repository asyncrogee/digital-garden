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

> [!info] SAME NAME `Methods` > `Methods` from the **_Parent_** `Class` with the SAME NAME as the **_Child `Class`_**, gets **OVERRIDE** by the **_Child `Method`_**
>
> - BUT, they need to have the **SAME METHOD SIGNATURE**
>   For example, this would result to a `FATAL ERROR!`
>
> ```php
> public function addSlice(string $slice): void
> {
> }
> ```
>
> ```php
> public function addSlice(int $slice):void
> {
> }
> // OR the return value
> public function addSlice(STRING $slice): int
> {
> }
> ```
>
> THIS DOESN'T APPLY TO `__construct()` METHOD!

> [!example] `parent::__construct()` > `__construct()` when appears on both `Class` files,
> the **_Parent_** `__construct()` is **OVERWRITTEN**
>
> ```php
> class Toaster
> {
> 	protected array $slices;
> 	protected int $size;
>
> 	public function __construct()
> 	{
> 		$this->slices = [];
> 		$this->size = 2;
> 	}
>
> 	public function addSlice(string $slice): void
> 	{
> 		if (count($this->slices) < $this->size) {
> 			$this->slices[] = $slice;
> 		}
> 	}
> }
> ```
>
> ```php
> class ToasterPro extends Toaster
> {
> 	public function __construct()
> 	{
> 		parent::__construct();
> 		$this->size = 4;
> 	}
>
> 	public function toastBagel()
> 	{
> 		// ...
> 	}
> }
> ```
>
> - the `__construct()` method here is run instead of the one from the **_Parent `Class`_**
>   - with `parent::construct()` we run the one from the **_Parent `Class`_** first,
>   - then Modified `size`
