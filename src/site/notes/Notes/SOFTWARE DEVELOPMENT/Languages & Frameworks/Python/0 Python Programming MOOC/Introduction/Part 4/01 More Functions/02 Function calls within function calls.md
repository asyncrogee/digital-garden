---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/0-python-programming-mooc/introduction/part-4/01-more-functions/02-function-calls-within-function-calls/","created":"2025-07-13T15:25:01.040+08:00"}
---

Author: [University of Helsinki](https://programming-23.mooc.fi/)
Type: Website
Topics: #python #mooc
Link: [Python Programming MOOC 2023](https://programming-23.mooc.fi/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
# 02 Function calls within function calls

--- 
You can call a function from within another function.

In the following example the function ___`greet_many_times`___ calls the function `greet` as many times as specified by the argument ___`times`___:

```python
def greet(name):
    print("Hello there,", name)

def greet_many_times(name, times):
    while times > 0:
        greet(name)
        times -= 1

greet_many_times("Emily", 3)
```