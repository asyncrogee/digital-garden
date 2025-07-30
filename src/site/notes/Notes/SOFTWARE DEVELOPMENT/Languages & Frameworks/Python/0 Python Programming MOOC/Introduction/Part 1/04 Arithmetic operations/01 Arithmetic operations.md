---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/0-python-programming-mooc/introduction/part-1/04-arithmetic-operations/01-arithmetic-operations/","created":"2025-07-13T15:25:00.341+08:00"}
---

Author: [University of Helsinki](https://programming-23.mooc.fi/)
Type: Website
Topics: #python #mooc #arithmeticoperations #numbers 
Link: [Python Programming MOOC 2023](https://programming-23.mooc.fi/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
# 01 Arithmetic operations

--- 
  

|Operator|Purpose|Example|Result|
|---|---|---|---|
|`+`|Addition|`2 + 4`|`6`|
|`-`|Subtraction|`10 - 2.5`|`7.5`|
|`*`|Multiplication|`-2 * 123`|`-246`|
|`/`|Division (floating point result)|`9 / 2`|`4.5`|
|`//`|Division (integer result)|`9 // 2`|`4`|
|`%`|Modulo|`9 % 2`|`1`|
|`**`|Exponentiation|`2 ** 3`|`8`|

The order of operations is familiar from mathematics: first calculate the exponents, then multiplication and division, and finally addition and subtraction. The order can be changed with parentheses.

For example this bit of code

```python
print(2 + 3 * 3)
print((2 + 3) * 3)
```