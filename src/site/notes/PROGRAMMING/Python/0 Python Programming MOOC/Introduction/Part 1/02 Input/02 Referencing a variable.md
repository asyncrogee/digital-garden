---
{"dg-publish":true,"permalink":"/programming/python/0-python-programming-mooc/introduction/part-1/02-input/02-referencing-a-variable/","created":"2024-11-09T11:30:52.289+08:00"}
---

Author: [University of Helsinki](https://programming-23.mooc.fi/)
Type: Website
Topics: #python #mooc #input #variables
Link: [Python Programming MOOC 2023](https://programming-23.mooc.fi/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
# Referencing a variable

--- 
A single variable can be referred to many times in a program:

```python
name = input("What is your name? ")

print("Hi, " + name + "!")
print(name + " is quite a nice name.")
```

If the user gives the name `Paul Python`, this program prints out the following:

```
What is your name? Paul Python 
Hi, Paul Python! 
Paul Python is quite a nice name.
```

Let's have a closer look at the way the `print` command is used above. Within the brackets of the command there is both text in quotation marks as well as variable names which refer to input from the user. These have been combined with a `+` operator, which _concatenates_ two strings into a single string.

Strings and variables can be combined quite freely:

```python
name = input("What is your name? ")

print("Hi " + name + "! Let me make sure: your name is " + name + "?")
```