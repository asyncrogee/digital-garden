---
{"dg-publish":true,"permalink":"/programming/web-development/backend/php/02-object-oriented-programming-oop/18-date-time-object/01-date-time-object/","tags":["programming","php","webdevelopment","backend","OOP"],"created":"2024-11-09T11:30:32.800+08:00"}
---


---

> [!tip] **Slashes** vs **_Dashes/Dots_**
>
> - **Slashes** on `Date` refers to **American/US `date` Format**
> - **_Dashes/Dot_** refers to **_Europeian Format_**

> [!info]
>
> ```php
> $dateTime = new DateTime('05/12/2021', new DateTimeZone('Europe/Amsterdam'));
>
>
> ```

> [!info] TimeZone
>
> ```php
> $dateTime = new DateTime('05/12/2021', new DateTimeZone('Europe/Amsterdam'));
>
> // OR
> $dateTime = newDateTime('05/12/2021');
>
> $dateTime->setTimezone(new DateTimeZone('Europe/Amsterdam'));
>
> echo $dataeTime->format('m/d/Y g:i A') . PHP_EOL;
>
> // GET TIMEZONE
> $dateTime->getTimezone()->getName();
> ```

> [!tip] Change date & time - `setDate()`, `setTime()`
>
> ```php
> $dateTime->setDate(2021, 4, 21)->setTime(2, 15);
> ```

> [!info] `DateTime::createFromFormat()`
> Create datetime objects from specific format
>
> ```php
> $date = '15/05/2021 3:30PM';
>
> $dateTime = DateTime::createFromFormat('d/m/Y g:iA', $date);
> ```
>
> ---
>
> `::creaFromFormat` uses the **CURRENT `TIME`** in the **_Timezone_** when not provided.
>
> ```php
> $date = '15/05/2021';
>
> $dateTime = DateTime::createFromFormat('d/m/Y', $date);
> var_dump($dateTime);
> ```
>
> ![Pasted image 20240330071600.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/18%20DateTime%20Object/attachments/Pasted%20image%2020240330071600.png)
> Compared when creating an `object`
>
> ```php
> var_dump($dateTime, new DateTime('15-05-2021'));
> ```
>
> ![Pasted image 20240330072420.png](/img/user/PROGRAMMING/Web%20Development/Backend/PHP/02%20Object-Oriented%20Programming%20(OOP)/18%20DateTime%20Object/attachments/Pasted%20image%2020240330072420.png)

> [!abstract] Compare dates
>
> ```php
> $dateTime1 = new DateTime('05/25/2021 9:15 AM');
> $dateTime2 = new DateTime('05/25/2021 9:14 AM');
>
> var_dump($dateTime1 < $dateTime2); // bool(false)
> var_dump($dateTime1 > $dateTime2); // bool(true)
> var_dump($dateTime1 == $dateTime2); // bool(false)
> var_dump($dateTime1 <==> $dateTime2); // int(1)
> ```

> [!tip] `DateInterval` Class
> Calculate **Difference between 2 Dates**
>
> ```php
> $dateTime1 = new DateTime('05/25/2021 9:15 AM');
> $dateTime2 = new DateTime('03/25/2021 9:14 AM');
>
> var_dump($dateTime1->diff($dateTime2));
>
> echo $dateTime1->diff($dateTime2)->days; // 71
> ```
