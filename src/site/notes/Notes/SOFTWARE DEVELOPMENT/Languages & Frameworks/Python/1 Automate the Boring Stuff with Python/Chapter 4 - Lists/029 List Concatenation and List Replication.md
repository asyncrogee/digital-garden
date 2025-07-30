---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/1-automate-the-boring-stuff-with-python/chapter-4-lists/029-list-concatenation-and-list-replication/","created":"2025-07-13T15:25:05.539+08:00"}
---

Author: [Alsweigart](https://alsweigart.com/)
Type: Book/Website
Topics: #python #list 
Link: [Automate boring stuff with Python](https://automatetheboringstuff.com/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] [[Notes/SOFTWARE DEVELOPMENT/Languages & Frameworks/Python/1 Automate the Boring Stuff with Python/Chapter 4 - Lists/023 List Data Type\|List]] 

---
# List Concatenation and List Replication

Lists can be concatenated and replicated just like strings.

To __COMBINE__ _two lists_ to create a new list value, use __plus__( ___+___ ) operator.
```python
concatenate = [1, 2, 3] + ['A', 'B', 'C']

print(concatenate)
```

To __REPLICATE__ a list, use __multiply__( ___*___ ) together with an _integer_ value.
```python
replicate = ['X', 'Y', 'Z'] * 3

print(replicate)
```

More:
```python
spam = [1, 2, 3]
spam = spam + ['A', 'B', 'C']

print(spam)
```