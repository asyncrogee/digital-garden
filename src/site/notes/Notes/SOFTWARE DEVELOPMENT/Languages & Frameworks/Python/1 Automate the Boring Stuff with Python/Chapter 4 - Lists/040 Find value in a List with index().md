---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/1-automate-the-boring-stuff-with-python/chapter-4-lists/040-find-value-in-a-list-with-index/","created":"2025-07-13T15:25:05.499+08:00"}
---

Author: [Alsweigart](https://alsweigart.com/)
Type: Book/Website
Topics: #python #list #methods
Link: [Automate boring stuff with Python](https://automatetheboringstuff.com/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]]  [[Notes/SOFTWARE DEVELOPMENT/Languages & Frameworks/Python/1 Automate the Boring Stuff with Python/Chapter 4 - Lists/023 List Data Type\|List]] [[Notes/SOFTWARE DEVELOPMENT/Languages & Frameworks/Python/1 Automate the Boring Stuff with Python/Chapter 4 - Lists/039 Methods\|Methods]] 

---
# Finding a Value in a List with the index() Method

List values have an ___index()___ method that can be __passed a value__,
and if that value __exists in the list__, the index of the value is __returned__.
If the value __isn’t in the list__, then Python produces a ___ValueError___ error.

```python
spam = ['hello', 'hi', 'howdy', 'heyas']
print(spam.index('hello'))

print(spam.index('heyas'))

print(spam.index('howdy howdy howdy'))
```

When there are __duplicates__ of the value in the list, the index of its __first appearance__ is returned.

```python
spam = ['Zophie', 'Pooka', 'Fat-tail', 'Pooka']
print(spam.index('Pooka'))
```