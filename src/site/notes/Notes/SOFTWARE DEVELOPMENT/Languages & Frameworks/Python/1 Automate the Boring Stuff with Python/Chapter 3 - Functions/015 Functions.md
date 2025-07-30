---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/1-automate-the-boring-stuff-with-python/chapter-3-functions/015-functions/","created":"2025-07-13T15:25:05.399+08:00"}
---

Author: [Alsweigart](https://alsweigart.com/)
Type: Book/Website
Topics: #python #functions
Link: [Automate boring stuff with Python](https://automatetheboringstuff.com/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
```python
def hello():
	print('Howdy!')  
     print('Howdy!!!')  
     print('Hello there.')

hello()  
hello()  
hello()
```

***def*** statement defines a **function**, in this case the **function** name is ***hello()***.
We **call the function** by typing the function name ***hello()***

The function is called ***three times***, so the code inside the **hello()** function is executed ***three times***.
# def Statements with Parameters

```python
def hello(name):  
	print('Hello, ' + name)  
  
hello('Alice')  
hello('Bob')
```
Function's like ***print()*** or ***len()***, you **pass values to them** called **arguments** by typing them **between the parentheses**.

- If you put the function ***hello(name)*** after ***hello('Bob')***, the program will give you a **NameError**