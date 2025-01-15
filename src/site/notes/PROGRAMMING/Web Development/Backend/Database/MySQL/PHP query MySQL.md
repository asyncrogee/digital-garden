---
{"dg-publish":true,"permalink":"/programming/web-development/backend/database/my-sql/php-query-my-sql/","tags":["programming","webdevelopment","backend","MySQL"],"created":"2024-11-09T11:30:31.261+08:00"}
---


#### Retrieve 1 row from a Table
```php
include("database.php");

$sql = "SELECT * FROM users WHERE user = 'Spongebob'";
$result = mysqli_query($conn, $sql);

if(mysqli_num_rows($result) > 0) {
	$row = mysqli_fetch_assoc($result);
	echo $row["id"] . "<br>";
	echo $row["user"] . "<br>";
	echo $row["reg_date"] . "<br>";
} else {
	echo "No user found".
}

mysqli_close($conn);
```