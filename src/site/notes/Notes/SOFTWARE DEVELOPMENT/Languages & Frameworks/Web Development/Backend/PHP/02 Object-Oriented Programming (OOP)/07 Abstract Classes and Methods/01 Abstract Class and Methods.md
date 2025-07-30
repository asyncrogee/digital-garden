---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/02-object-oriented-programming-oop/07-abstract-classes-and-methods/01-abstract-class-and-methods/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2025-07-13T15:24:54.924+08:00"}
---


---

> [!info] Abstract Class
>
> - Can't instantiate `abstract classes`
>   - **_CANT CREATE_** `OBJECT`
>   - **CAN ONLY BE** `EXTENDED`
> - Have the `Method`'s **Signature** and **definition**
>   - but **_NOT_** the actual **_IMPLEMENTATION_**
> - the **_IMPLEMENTATION_** is done in the `CHILD CLASSES`
>   > [!note]
>   > A `class` is a _BLUEPRINT_ for an **object**
>   > an `ABSTRACT class` is a _BLUEPRINT_ for its **CHILD CLASSes**
>   >
>   > `ABSTRACT` can only be **PUBLIC** or **PROTECTED**
>   > since it is needed by it's `Child Classes`

> [!example] >_Index.php_
>
> ```php
> require_once __DIR__ .'/../vendor/autoload.php';
>
> $fields = [
> 	new \App\Text('textField'),
> 	new \App\Checkbox('checkboxField'),
> 	new \App\Radio('radioField'),
> ];
>
> foreach($fields as $field) {
> 	echo $field->render() . '<br />';
> }
> ```
>
> _Field.php_
>
> ```php
> namespace App;
>
> abstract class Field
> {
> 	public function __construct(protected string $name)
> 	{
>
> 	}
>
> 	abstract public function render(): string;
> }
> ```
>
> _Text.php_:
> for Text Fields
>
> ```php
> namespace App;
>
> class Text extends FIeld
> {
> 	public function render(): string
> 	{
> 		return <<<HTML
> 		<input type="text" name="{$this->name}" />
> 		HTML;
> 	}
> }
> ```
>
> _Boolean.php_
> for boolean fields (`true/false`, `on/off`)
>
> ```php
> namespace App;
>
> abstract class Boolean extends Field
> {
>
> }
> ```
>
> _Checkbox.php_
>
> ```php
> namespace App;
>
> class Checkbox extends Boolean
> {
> 	public function render(): string
> 	{
> 		return <<<HTML
> 		<input type="checkbox" name="{$this->name}" />
> 		HTML;
> 	}
> }
> ```
>
> _Radio.php_
>
> ```php
> namespace App;
>
> class Checkbox extends Boolean
> {
> 	public function render(): string
> 	{
> 		return <<<HTML
> 		<input type="radio" name="{$this->name}" />
> 		HTML;
> 	}
> }
> ```
