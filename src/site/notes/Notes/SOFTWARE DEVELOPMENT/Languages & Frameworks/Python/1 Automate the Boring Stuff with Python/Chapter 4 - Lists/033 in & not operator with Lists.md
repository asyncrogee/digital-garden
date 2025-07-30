---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/1-automate-the-boring-stuff-with-python/chapter-4-lists/033-in-and-not-operator-with-lists/","created":"2025-07-13T15:25:05.523+08:00"}
---

Author: [Alsweigart](https://alsweigart.com/)
Type: Book/Website
Topics: #python #list #in #not
Link: [Automate boring stuff with Python](https://automatetheboringstuff.com/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] [[Notes/SOFTWARE DEVELOPMENT/Languages & Frameworks/Python/1 Automate the Boring Stuff with Python/Chapter 4 - Lists/023 List Data Type\|List]] 

---
# The in and not in Operators

To determine whether a value __is or isn’t in a list__ with the ___in___ and ___not___ in operators.

These expressions will evaluate to a __Boolean value__.

```python
'howdy' in ['hello', 'hi', 'howdy', 'heyas']

spam = ['hello', 'hi', 'howdy', 'heyas']
'cat' in spam

'howdy' not in spam
'cat' not in spam
```

This code will check whether the pet name the user inputted is in the list:
```python
myPets = ['Zophie', 'Pooka', 'Fat-tail']  
print('Enter a per name:')  
name = input()  
  
if name not in myPets:  
	print('I do not have a pet named ' + name)  
else:  
	print(name + ' is my pet.')
```