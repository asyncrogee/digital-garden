---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/0-python-programming-mooc/introduction/part-4/02-lists/02-accessing-items-in-a-list/","created":"2025-07-13T15:25:05.651+08:00"}
---

Author: [University of Helsinki](https://programming-23.mooc.fi/)
Type: Website
Topics: #python  #mooc #list  #introduction
Link: [Python Programming MOOC 2023](https://programming-23.mooc.fi/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
## Accessing items in a List

The items in a list are indexed in exactly the same way as characters in a string.
Indexing starts from ___zero___, and the last index is the length of the list ___minus 1___:

![[Pasted image 20230812164052.png]]
A single list item can be accessed just like a single character in a string is accessed, with square brackets:
```python
my_list = [7, 2, 2, 5, 2]

print(my_list[0])
print(my_list[1])
print(my_list[3])

print("The sum of the first two items:", my_list[0] + my_list[1])
```

The entire contents of the list can also be printed out:

```python
my_list = [7, 2, 2, 5, 2]
print(my_list)
```

Unlike strings, __lists are mutable__, which means their _contents can change_. 
You can assign a new value to an item within a list, just like you can assign a new value to a variable:
```python
my_list = [7, 2, 2, 5, 2]
print(my_list)
my_list[1] = 3
print(my_list)
```

The function `len` gives you the number of items in a list:
```python
my_list = [7, 2, 2, 5, 2]
print(len(my_list))
```

