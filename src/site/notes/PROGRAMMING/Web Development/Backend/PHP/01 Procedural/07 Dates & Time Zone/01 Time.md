---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/01-procedural/07-dates-and-time-zone/01-time/","tags":["programming","php","webdevelopment","backend"]}
---


--- 




> [!info] Time
> Prints numbers of __Seconds__ since `January 1, 1970`:
> ```php
> $currentTime = time();
> 
> echo $currentTime; // example: 1611000638
> echo $currentTime + 5 * 24 * 60 * 60; // Time in 5 DAYS: 1611432638
> echo $currentTime - 60 * 60 * 24; // Time Yesterday: 1610914238
> 
> ```

>[!info] Date
>Format Characters: https://www.php.net/manual/en/datetime.format.php
>- __First__ argument is the __FORMAT__
>- ___Second___ argument is the ___TIMESTAMP___
>
>```php
>
>
>echo date('m/d/Y g:ia');
>
>echo date('m/d/Y g:ia', $currentTime + 5 *24 * 60 * 60);
>```

> [!info] Timezone
> ```php
> echo date_default_timezone_set('UTC');
> echo date_default_timezone_get(); // CURRENT TIME ZONE
> ```

> [!tip] mktime
> Get unix timestamp based on arguments:
> ```php
>echo mktime(0, 0, 0, 4, 10, null); // 1618027200
>echo date('m/d/Y g:ia', mktime(0, 0, 0, 4, 10, null)); // 4/10/2021 12:00am
> ```
> - `4`th Month
> - `10`th Day
> - `null` for __Current Year__

> [!tip] strtotime
> ```php
> echo strtotime('2017-01-10 07:00:00'));
> 
> echo date('m/d/Y g:ia, strtotime('2021-01-18 07:00:00'));
> echo date('m/d/Y g:ia, strtotime('tomorrow'));
> echo date('m/d/Y g:ia, strtotime('first day of february'));
> echo date('m/d/Y g:ia, strtotime('last day of february'));
> echo date('m/d/Y g:ia, strtotime('first day of february 2020'));
> echo date('m/d/Y g:ia, strtotime('second friday of January'));
> ```

> [!info] Date Parse
> Returns an `array` containing __Details__ about the __DATE__
> ```php
> $date =  date('m/d/Y g:ia, strtotime('second friday of January'));
> print_r(date_parse($date));
> ```
> ![Pasted image 20240316100257.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/01%20Procedural/07%20Dates%20&%20Time%20Zone/attachments/Pasted%20image%2020240316100257.png)
> Parse the __Date__ from specific `format`:
> ```php
> print_r(date_parse_from_format('m/d/Y g:ia', $date));
> ```
> Same from the above: 
> ![Pasted image 20240316100324.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/01%20Procedural/07%20Dates%20&%20Time%20Zone/attachments/Pasted%20image%2020240316100324.png)
