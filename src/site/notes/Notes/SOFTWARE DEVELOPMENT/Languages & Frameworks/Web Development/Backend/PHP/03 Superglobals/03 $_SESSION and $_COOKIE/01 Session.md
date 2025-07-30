---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/03-superglobals/03-session-and-cookie/01-session/","tags":["programming","php","webdevelopment","backend","SUPERGLOBALS"],"created":"2025-07-13T15:24:55.374+08:00"}
---


---

> [!info]
>
> - **SESSIONS** :
>   - Stored in Server Side
>   - Destroyed upon closing the browser
> - **_COOKIES_** :
>   - Stored in Client Side
>   - Remain as long as the `Expiration date`
>     - Or when **_cookies_** are deleted.

> [!info] **SESSIONS**
>
> - Must be started **before any `Output`**
>
> ```php
> session_start();
> ```
>
> - When **Session** is started, it **creates a `Unique Session ID`** - and it writes it on **_Cookie_**
>   ![[Pasted image 20240330164729.png]]
>   ![[Pasted image 20240330164826.png]]
>
> > [!tip]
> > _Home.php_
> >
> > ```php
> > declare(strict_types=1);
> >
> > namespace App\Classes;
> >
> > user App\View;
> >
> > class Home
> > {
> > 	public function index(): string
> > 	{
> > 		$_SESSION['count'] = ($_SESSION['count'] ?? 0) + 1;
> > 		return View::make('index', $_GET)->render();
> > 	}
> > }
> > ```
> >
> > _index.php_
> >
> > ```php
> > session_start();
> >
> > $router = new App\Router();
> >
> > $router
> > 	->get('/', [App\Classes\Home::class, 'index'])
> > 	->get('/invoices', [App\Classes\Invoice::class, 'index'])
> > 	->get('/invoices/create', [App\Classes\Invoice::class, 'create'])
> > 	->post('/invoices/create', [App\Classes\Home::class, 'store']);
> >
> > echo $router->resolve(
> > 	$_SERVER['REQUEST_URL'],
> > 	strtolower($_SERVER['REQUEST_METHOD'])
> > );
> >
> > var_dump($_SESSION);
> > ```
> >
> > - Everytime _Home_ Page is visited/reloaded, the **Counter** INCREMENTS
> >   - It can be removed by deleting the **_Cookie_**
> >   - Or using `unset` on it
> >
> > ```php
> > unser($_SESSION['count']);
> > ```




> [!info]
> A Super Global Variable
> - Used to ___store information on a user___ to be __used across multiple pages__.
> 	- A user is assigned a `session-id`
> EXAMPLE:
> - Login Credentials


Before the `HTML code`:

__Session__ should be STARTED FIRST
```php
<?php
	session_start();
?>

// HTML CODE

<?php

?>
//php again
```

> [!example]
> 2 php files
> File 1: `index.php`
> ```php
> <?php
> 	session_start();
> ?>
> 
> // HTML CODE
> 
> <?php
> $_SESSION["username"] = "BroCode";
> $_SESSION["password"] = "pizza123";
> 
> echo $_SESSION["username"] . "<br>";
> echo $_SESSION["password"] . "<br>";
> ?>
> ```
> 
> File 2: `home.php`
> 
> <?php
> session_start();
> ?>
> ```php
> <?php
> 	session_start();
> ?>
> // HTML CODE
> 
> <? php
> echo $_SESSION["username"] . "<br>";
> echo $_SESSION["password"] . "<br>";
> ?>
> ```

---


> [!example]
> 
> File 1: `index.php`
> ```php
> <?php
> session_start(); 
> ?>
> 
> // HTML
> <body>
> 	 <form action = "index.php" method = "post"> 
> 		 username: <br>
> 		 <input type = "text" name="username"><br>
> 		 password: <br>
> 		 <input type="password" name="password"><br>
> 		 <input type="submit" name="login" value="login">
> 	 </form>
> </body>
> 
> <?php
> if(isset($_POST["login"])){ // IF login button is clicked
> 	if(!empty($_POST["username"]) && 
> 		!empty($_POST["password"])) { // And Username and Password field is NOT EMPTY
> 			$_SESSION["username"] = $_POST["username"]; // Assign Username
> 			$_SESSION["password"] = $_POST["password"]; // and Password to SESSION
> 		
> 			header("Location: home.php"); // REDIRECTS to home.php
> 		} else {
> 			echo "Missing username/password <br>"
> 		}
> }
> ?>
> ```
> 
> File 2: `home.php`
> ```php
> <?php 
> session_start();
> ?>
> 
> // HTML
> <form action="home.php" method="post">
> 	<input type="submit" name="logout" value="logout">
> </form>
> 
> <?php
> 	 echo $_SESSION["username"] . "<br>";
> 	 echo $_SESSION["password"] . "<br>";
> 	 
> 	 if(isset($_POST["logout"])) {
> 		 session_destroy();
> 		 header("Location: index.php");
> 	 }
> ?>
> ```

