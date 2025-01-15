---
{"dg-publish":true,"permalink":"/programming/web-development/backend/database/my-sql/my-sql/","tags":["programming","webdevelopment","backend","MySQL"],"created":"2024-11-09T11:30:26.109+08:00"}
---


https://youtu.be/mSnte-Ovm10?si=xTzDIVtQAQAowojS


> [!info] Select the `DATABASE`
>```SQL
>use my_db;
>```

> [!INFO] Create `TABLE`
> ```SQL
> CREATE TABLE users (
> 	id int UNSIGNED PRIMARY KEY AUTO_INCREMENT,
> 	email varchar(255) UNIQUE NOT NULL,
> 	full_name varchar(255) NOT NULL,
> 	is_active boolean DEFAULT 0 NOT NULL,
> 	created_at datetime NOT NULL,
> 	KEY `is_active`(`is_active`)
> );
> ```

>[!tip] Get information about the `TABLE`
>```sql
>describe users
>```

