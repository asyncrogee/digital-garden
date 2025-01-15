---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/javascript-vanilla/02-code-quality/02-coding-style/","tags":["programming","webdevelopment","frontend","JavaScript"],"created":"2024-11-09T11:30:39.053+08:00"}
---

## Clean Code Cheat Sheet
--- 
![Pasted image 20240108230702.png](/img/user/PROGRAMMING/Web%20Development/FrontEnd/Javascript%20(Vanilla)/02%20Code%20quality/attachments/Pasted%20image%2020240108230702.png)


---
## Line Length

--- 
It's best practice to split long horizontal line of code.
```javascript
// backtick quotes `` allow to split the string into multiple lines
let str = `
	ECMA International's TC39 is a group of JavaScript developers, implementers, academics, and more, collaborating with the community to maintain and evlve the definition of JavaScript.
`;

```

for `if` statements:
```javascript
if (
  id === 123 &&
  moonPhase === 'Waning Gibbous' &&
  zodiacSign === 'Libra'
) {
  letTheSorceryBegin();
}
```


---
## Nesting Levels
---
Try to avoid nesting code too many levels deep.


>[!example] Examples:
>Option 1:
>``` javascript
>function pow(x, n) {
>	if (n < 0) {
>		alert("Negative 'n' not supported");
>	} else {
>		let result = 1;
>		
>		for (let i = 0; i < n; i++) {
>			result *= x;
>		}
>		
>		return result;
>	}
>}
>```
>Option 2:
>```javascript
>function pow(x, n) {
>	if (n < 0) {
>		alert("Negative 'n' not supported");
>		return;
>	}
>	
>	let result = 1;
>	
>	for (let i = 0; i < n; i++) {
>		result *= x;
>	}
>	
>	return result;
>}
>```
