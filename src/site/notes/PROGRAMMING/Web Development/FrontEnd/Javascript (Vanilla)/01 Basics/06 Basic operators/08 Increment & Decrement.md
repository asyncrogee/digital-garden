---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/01-basics/06-basic-operators/08-increment-and-decrement/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:42.339+08:00"}
---


# Increment & Decrement

---

Increasing and Decreasing a number by one

- **Increment** `++` increases a variable by 1:

```javascript
let counter = 2;
counter++; // wors the same as counter = counter + 1
alert(counter); // 3
```

- **Decrement** `--` decreases a variable by 1:

```javascript
let counter = 2;
counter--; // works the same as counter = counter - 1
alert(counter); // 1
```

> [!Caution]
> Increment/Decrement can only be applied to variables
>
> - `5++` will give an **_error_**

The operators `++` and `--` can be placed either before or after a variable.

- **Prefix form** - `++counter`

  - returns the new value

  ```javascript
  let counter = 1;
  let a = ++conter; // (*)

  alert(a); // 2
  ```

````

- __Postfix form__ - `counter++`
	- returns the old value
	```javascript
	let counter = 1;
	let a = counter++; // (*) changed ++counter to counter++

	alert(a)
````

> [!question]- Why use Postfix?
> Using it will lessened the hassle of calculating and incrementing:
>
> ```javascript
> let counter = 1;
> alert(2 * counter);
> counter++;
> alert(counter);
> ```
>
> Shorten:
>
> ```Javascript
> let counter = 1;
> alert( 2 * counter ++ );
> alert(counter)
> ```
>
> Basically, it just makes it shorter

> [!EXAMPLES] Summary:
>
> - If the result is not used, there's no difference in which form to use:
>
> ```javascript
> let counter = 0;
> counter++;
> ++counter;
> alert(counter); // 2, the lines above did the same
> ```
>
> - Increase value and immediately use the result
>   - use **Prefix form**:
>
> ```javascript
> let counter = 0;
> alert(++counter); // 1
> ```
>
> - Increment a value but use its previous value,
>   - use **Postfix** form:
>
> ```javascript
> let counter = 0;
> alert(counter++); // 0
> ```

> [!TIP] Increment/Decrement among other operators
>
> ```javascript
> let counter = 1;
> alter(2 * ++counter); // 4
> ```
>
> Compare with:
>
> ```javascript
> let counter = 1;
> alert(2 * counter++); // 2, because counter++ returns the "old" value
> ```
