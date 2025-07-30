---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/08-interfaces-and-polymorphism/01-interfaces-and-polymorphism/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.956+08:00"}
---


---

> [!info] Interface
>
> - Interface tells **WHAT NEEDS TO BE DONE**
> - but **_DOESN'T TELL the IMPLEMENTATION on HOW IT'S NEED TO BE DONE_**
>   > [!example]
>   > Non-Technical Example:
>   > ![[Pasted image 20240328181217.png]]
>   >
>   > - There's different **Debt Collectors**
>   >   - with **_Different Method of `COllecting Money`_**
>   > - You don't care **HOW they COLLECT THE MONEY**
>   >   - As long as, you GET THE MONEY, or a portion of it.

> [!abstract] Interface Rules
>
> - **ALL `METHODS`** within **_Interface_** **MUST BE `PUBLIC`**
> - ALL `Methods` within the **_INTERFACE_** **MUST BE IMPLEMENTED** to the class that **implements** that **_interface_**
> - **_Intefaces_** CANNOT HAVE `Properties`
>   - but IT CAN HAVE **CONSTANTS**

> [!info] Polymorphism
>
> - Means **Many Forms**
> - An `Object` is considered **Polymorphic** if it **CAN PASS MULTIPLE INSTANCES**
> - Which indicates that it can take many forms

> [!example]
> _Index.php_
>
> ```php
> require_once __DIR__ . '/../vendor/autoload.php';
>
> $collector = new \App\CollectionAgency();
>
> echo $colector->collect(100) . PHP_EDL;
> ```
>
> _DebtCollector.php_
>
> ```php
> namespace App;
>
> interface DebtCollector
> {
>
> 	public function __construct();
> 	public function collect(float $owedAmount): float;
> }
> ```
>
> _DebtCollectorService.php_
>
> ```php
> namespace App;
>
> class DebtCollectionService
> {
> 	public function collectDebt(DebtCollector $collector)
> 	{
> 		$owedAmount = mt_rand(100, 1000);
> 		$collectedAmount = $collector->collect($owedAmount);
>
> 		echo 'Collected 
>
> _CollectionAgency.php_
>
> ```php
> namespace App;
>
> class CollectionAgency implements DebtCollector
> {
> 	public function collect(float $owedAmount): float
> 	{
> 		$guaranteed = $owedAmount * 0.5;
>
> 		return mt_rand($guaranteed, $owedAmount);
> 	}
> }
> ```
>
> _Rocky.php_
>
> ```php
> namespace App;
>
> class Rocky implements DebtCollector
> {
> 	public function collect(float $owedAmount): float
> 	{
>
>
> 		return $owedAmount * 0.65;
> 	}
> }
> ```
>
> - Multiple `Interfaces` can be Implemented
> - `mt_rand` generates a random number
>   - `mt_rand(minimum, maximum);`

> [!tip] **_Interface_** can also **Extend**
>
> ```php
> namespace App;
>
> interface DebtCollector extends AnotherInterface, SomeOtherInterface
> {
> 	public function __construct();
> 	pubic function collect(float $owedAmount): float;
> }
> ```
>
> - `Concrete Class` will need to **Implement** all the `methods` from the **_Interface_** and it's **Extensions**
 . $collectedAmount . ' out of 
>
> _CollectionAgency.php_
>
> {{CODE_BLOCK_3}}
>
> _Rocky.php_
>
> {{CODE_BLOCK_4}}
>
> - Multiple `Interfaces` can be Implemented
> - `mt_rand` generates a random number
>   - `mt_rand(minimum, maximum);`

> [!tip] **_Interface_** can also **Extend**
>
> {{CODE_BLOCK_5}}
>
> - `Concrete Class` will need to **Implement** all the `methods` from the **_Interface_** and it's **Extensions**
 . $owedAmount . PHP_EDL;
> 	}
>
> }
> ```
>
> _CollectionAgency.php_
>
> {{CODE_BLOCK_3}}
>
> _Rocky.php_
>
> {{CODE_BLOCK_4}}
>
> - Multiple `Interfaces` can be Implemented
> - `mt_rand` generates a random number
>   - `mt_rand(minimum, maximum);`

> [!tip] **_Interface_** can also **Extend**
>
> {{CODE_BLOCK_5}}
>
> - `Concrete Class` will need to **Implement** all the `methods` from the **_Interface_** and it's **Extensions**
