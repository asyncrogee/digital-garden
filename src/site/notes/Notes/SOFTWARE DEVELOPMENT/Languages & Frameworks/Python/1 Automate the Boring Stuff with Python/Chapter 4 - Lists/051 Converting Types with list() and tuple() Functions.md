---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/1-automate-the-boring-stuff-with-python/chapter-4-lists/051-converting-types-with-list-and-tuple-functions/","created":"2025-07-13T15:25:05.459+08:00"}
---

Author: [Alsweigart](https://alsweigart.com/)
Type: Book/Website
Topics: #python #list #tuple
Link: [Automate boring stuff with Python](https://automatetheboringstuff.com/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] [[Notes/SOFTWARE DEVELOPMENT/Languages & Frameworks/Python/1 Automate the Boring Stuff with Python/Chapter 4 - Lists/023 List Data Type\|List]] 

---
# Converting Types with list() and tuple() Functions

Just like how ___str(42)___ will return ___'42'___, the string representation of the integer ___42___,

the functions ___list()___ and ___tuple()___ will return list and tuple versions of the values of the values passed to them.

```python
tuple(['cat', 'dog', 5])

list(('cat', 'dog', 5))

list('hello')
```

> Converting a tuple to a list is handy if you need a _mutable version_ of a __tuple__ value.