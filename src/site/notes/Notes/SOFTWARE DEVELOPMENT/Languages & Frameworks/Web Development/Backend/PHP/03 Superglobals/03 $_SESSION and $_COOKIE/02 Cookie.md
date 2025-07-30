---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/backend/php/03-superglobals/03-session-and-cookie/02-cookie/","tags":["programming","php","webdevelopment","backend","SUPERGLOBALS"],"created":"2025-07-13T15:24:55.370+08:00"}
---


---

> [!abstract] Cookies
> A file that is stored in the user's computer
> Used for:
>
> - Session Management
> - Tracking Targeted Ads
> - Store Information to enhance User's Experience on the Website
>
> **SET THE `COOKIE` BEFORE ANY OUTPUT!!!** > **_DONT STORE `SENSITIVE DATA` TO `COOKIES`_**
> 
> Information about a `user` stored in a user's web-browser
> Examples: 
> - Targeted Advertisements,
> - Browsing Preferences
> - Other non-sensitive data

> [!info]
> Creating a **_Cookie_**
>
> ```php
> setcookie(
> 	`userName`,
> 	'Gio',
> 	time() + 10,
> 	'/',
> 	'',
> 	false,
> 	false
> );
> ```
>
> `setcookie` **Arguments**:
>
> - 1st`userName`: Name of the **_Cookie_**
> - 2nd`'Gio'`: Value
> - 3rd`time() + 10`: EXPIRATION
> - 4th`'/'`: Which **Directory** the **_Cookie_** will be **VALID**
> - 5th`''`: Domain (Which domain should the **_cookie_** be available on.)
>   - If put on the **TOP LEVEL DOMAIN** (`mysite.com` for example) **it will be also available to all of it's** _SUB-DOMAIN_
> - 6th`false`: Secure Parameter (Whether should the **_cookie_** be sent ONLY over **Secure parameter** (`https` connection))
> - 7th`false`: HTTP only (If set to **True**, the **_cookie_** can ONLY be accessed by a **http protocol**)
>   - and **CANNOT be ACCESSED** by `Client-Side Code` like _JAVASCRIPT_
>
> ```php
> setcookie(
> 	`userName`,
> 	'Gio',
> 	time() + (24 * 60 * 60)
> );
> ```



```php

setcookie("fav_food", "pizza", time() + (86400 * 2), "/"); // Expires in 2 days
setcookie("fav_drink", "coffee", time() + (86400 * 3), "/"); // Expires in 3 days
setcookie("fav_food", "ice cream", time() + (86400 * 4), "/"); // Expires in 4 days
```

#### Deleting Cookies
```php
setcookie("fav_food", "pizza", time() - 0, "/");
```

#### Printing `key` & `value` pair from COOKIES

```php
foreach($_COOKIE as $key => $value) {
	echo "{$key} = {$value} <br>";
}
```
output:
![[Pasted image 20240320130009.png\|Pasted image 20240320130009.png]]
EXAMPLE:
```php
if(isset($_COOKIE["fav_food"])) {
	echo "BUY SOME {$_COOKIE["fav_food"]} !!!";
} else {
	echo "I don't know you favorite food"
}
```