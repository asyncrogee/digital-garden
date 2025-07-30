---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/1-automate-the-boring-stuff-with-python/chapter-3-functions/016-terms-define-call-pass-argument-parameter/","created":"2025-07-13T15:25:05.395+08:00"}
---

Author: [Alsweigart](https://alsweigart.com/)
Type: Book/Website
Topics: #python #terms
Link: [Automate boring stuff with Python](https://automatetheboringstuff.com/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] [[Notes/SOFTWARE DEVELOPMENT/Languages & Frameworks/Python/1 Automate the Boring Stuff with Python/Chapter 3 - Functions/015 Functions\|Functions]] 

---
# Define, Call, Pass, Argument, Parameter
```python
def sayHello(name):
	print('Hello, ' + name)
sayHello('Al')
```
- **define**-ing a function means to create it, the ***def*** statement defines ***sayHello()*** function.
- **call**, we call the created function like ***sayHello('Al')***, executing the function ***sayHello(name)***, and PASSING the string value ***'Al'*** to the function.
- **argument** - the value being passed **to a function in a function call**, the argument ***'Al'*** is assigned to a local variable named ***name***. 
- **parameters** - **Variables** that have **arguments** assigned to them are _parameters_.
- **expressions** are composed of values and operators. A **function call** can be used in an **expression** because the call evaluates to its return value.