---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/03-superglobals/04-file/01-file/","tags":["programming","php","webdevelopment","backend","SUPERGLOBALS"],"created":"2024-11-09T11:30:31.131+08:00"}
---


---

> [!info]
>
> ```php
> declare(strict_types = 1);
>
> namespace App\Classes;
>
> class Home
> {
> 	public function index(): string
> 	{
> 		return <<<FORM
> 		<form action="/upload" method="post" enctype="multipart/form-data">
> 			<input type="file" name="receipt" />
> 			<button type="submit">Upload</button>
> 		</form>
> 		FORM;
> 	}
>
> 	public function upload()
> 	{
> 		echo '<pre>';
> 		var_dump($_FILES);
> 		echo '</pre>';
> 	}
> }
> ```
>
> **_OUTPUT_** of the `var_dump($_FILES);`
> ![Pasted image 20240330172943.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/03%20Superglobals/04%20$_FILE/attachments/Pasted%20image%2020240330172943.png)
>
> _index.php_
>
> ```php
> session_start();
>
> $router = new App\Router();
>
> $router
> 	->get('/', [App\Classes\Home::class, 'index'])
> 	->post('/upload', [App\Classes\Home::class, 'upload'])
> 	->get('/invoices', [App\Classes\Invoice::class, 'index'])
> 	->get('/invoices/create', [App\Classes\Invoice::class, 'create'])
> 	->post('/invoices/create, [App\Classes\Invoice::class, 'store']);
>
> echo $router->resolve(
> 	$_SERVER['REQUEST_URI'],
> 	strtolower($_SERVER['REQUEST_METHOD'])
> );
> ```

> [!tip] Where are the FILES stored?
> ![Pasted image 20240330174342.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/03%20Superglobals/04%20$_FILE/attachments/Pasted%20image%2020240330174342.png) > `Files` uploaded in PHP are stored TEMPORARILY in the server's **default tmp directory**
>
> > Can be changed in `php ini configuration file`
>
> - In the end of the request, `files` from the **tmp directory** are **_DELETED_**
>   - Upload `files` to the CLOUD like **S3**
>   - or Local Directory
>
> ```php
> $filePath = STORAGE_PATH . '/' . $_FILES['receipt']['name'];
>
> move_uploaded_file($_FILES['receipt']['tmp_name'], $filePath);
>
> echo '<pre>';
> var_dump(pathinfo($filePath));
> echo '</pre>';
> ```
>
> _index.php_ or the **Main Application `Class`**:
>
> ```php
> define('STORAGE_PATH', __DIR__, '/../storage');
> ```
>
> **_OUTPUT_**:
> ![Pasted image 20240330180444.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/03%20Superglobals/04%20$_FILE/attachments/Pasted%20image%2020240330180444.png)
>
> -**Storage Path** - Could either be Hard-Coded - or Create a `constant` in the **Main Application `Class`**

> [!example] Upload **MULTIPLE FILES**
>
> ```php
> declare(strict_types = 1);
>
> namespace App\Classes;
>
> class Home
> {
> 	public function index(): string
> 	{
> 		return <<<FORM
> 		<form action="/upload" method="post" enctype="multipart/form-data">
> 			<input type="file" name="receipt" />
> 			<input type="file" name="myimage" />
> 			<button type="submit">Upload</button>
> 		</form>
> 		FORM;
> 	}
>
> 	public function upload()
> 	{
> 		echo '<pre>';
> 		var_dump($_FILES);
> 		echo '</pre>';
>
> 		$filePath = STORAGE_PATH . '/' . $_FILES['receipt']['name'];
>
> 		move_uploaded_file($_FILES['receipt']['tmp_name'], $filePath);
>
> 		echo '<pre>';
> 		var_dump(pathinfo($filePath));
> 		echo '</pre>';
> 	}
> }
> ```
>
> **_OUTPUT_**:
> ![Pasted image 20240330182507.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/03%20Superglobals/04%20$_FILE/attachments/Pasted%20image%2020240330182507.png)
>
> > [!tip] Storing in an `Array`
> >
> > ```php
> >  // ...
> > class Home
> > {
> > 	public function index(): string
> > 	{
> > 		return <<<FORM
> > 		<form action="/upload" method="post" enctype="multipart/form-data">
> > 			<input type="file" name="receipt[]" />
> > 			<input type="file" name="receipt[]" />
> > 			<button type="submit">Upload</button>
> > 		</form>
> > 		FORM;
> > 	}
> > 	// ...
> > ```
> >
> > - Added Square brackets `[ ] ` on the `name=""` >> **_OUTPUT_**:
> >   ![Pasted image 20240330183337.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/03%20Superglobals/04%20$_FILE/attachments/Pasted%20image%2020240330183337.png)
