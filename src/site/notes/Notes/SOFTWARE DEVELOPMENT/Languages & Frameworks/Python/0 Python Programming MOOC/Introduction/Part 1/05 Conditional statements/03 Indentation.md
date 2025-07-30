---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/0-python-programming-mooc/introduction/part-1/05-conditional-statements/03-indentation/","created":"2025-07-13T15:25:00.370+08:00"}
---

Author: [University of Helsinki](https://programming-23.mooc.fi/)
Type: Website
Topics: #python #mooc #indentation
Link: [Python Programming MOOC 2023](https://programming-23.mooc.fi/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
# 03 Indentation

--- 
Python recognises that a block of code is part of a conditional statement if each line of code in the block is _indented_ the same. That is, there should be a bit of whitespace at the beginning of every line of code within the code block. Each line should have the same amount of whitespace.

For example:

```python
password = input("Please type in a password: ")

if password == "kittycat":
    print("You knew the password!")
    print("You must be either the intended user...")
    print("...or quite an accomplished hacker.")

print("The program has finished its execution. Thanks and bye!")
```

You can use the Tab key, short for _tabulator_ key, to insert a set amount of whitespace.

![[Pasted image 20230828171749.png]]
Many text editors will automatically indent the following line when the Enter key is pressed after a colon character. When you want to end an indented code block you can use the `Backspace` key to return to the beginning of the line.
![[Pasted image 20230828171756.png]]
