---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/0-python-programming-mooc/introduction/part-2/03-combining-conditions/02-combining-and-chaining-conditions/","created":"2025-07-13T15:25:00.466+08:00"}
---

Author: [University of Helsinki](https://programming-23.mooc.fi/)
Type: Website
Topics: #python #mooc #combiningconditions 
Link: [Python Programming MOOC 2023](https://programming-23.mooc.fi/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
# 02 Combining and chaining conditions

--- 
The following program asks the user to type in four numbers. It then works out which of the four is the greatest, with the help of some conditions:

```python
n1 = int(input("Number 1: "))
n2 = int(input("Number 2: "))
n3 = int(input("Number 3: "))
n4 = int(input("Number 4: "))

if n1 > n2 and n1 > n3 and n1 > n4:
    greatest = n1
elif n2 > n3 and n2 > n4:
    greatest = n2
elif n3 > n4:
    greatest = n3
else:
    greatest = n4

print(f" {greatest} is the greatest of the numbers.")
```
In the above example the first condition ___`n1 > n2 and n1 > n3 and n1 > n4`___ is true only if all three conditions within are true.