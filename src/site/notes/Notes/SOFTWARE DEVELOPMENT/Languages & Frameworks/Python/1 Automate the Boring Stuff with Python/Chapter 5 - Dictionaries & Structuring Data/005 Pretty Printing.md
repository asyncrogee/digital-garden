---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/1-automate-the-boring-stuff-with-python/chapter-5-dictionaries-and-structuring-data/005-pretty-printing/","created":"2025-07-13T15:24:56.704+08:00"}
---

Author: [Alsweigart](https://alsweigart.com/)
Type: Book/Website
Topics: #python 
Link: [Automate boring stuff with Python](https://automatetheboringstuff.com/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
# pprint
Contains:
- `pprint()`
- `pformat()` 
that will "pretty print" a dictionary's values.

```python
import pprint
message = 'It was a  bright cold day in April, and the clocks were striking thirteen.'
count = {}

for character in message:
	count.setdefault(character, 0)
	count[character] = count[character] + 1

pprint.pprint(count)
```

## String instead of Display
Obtain prettified text as `string` instead of displaying it on the screen, call `pprint.pfomat()`
```python
pprint.pprint(someDictionaryValue)
print(pprint.pformat(someDictionaryValue))
```

