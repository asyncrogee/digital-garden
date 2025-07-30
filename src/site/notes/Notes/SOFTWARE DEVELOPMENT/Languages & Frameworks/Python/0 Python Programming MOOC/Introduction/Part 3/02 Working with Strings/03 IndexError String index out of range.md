---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/0-python-programming-mooc/introduction/part-3/02-working-with-strings/03-index-error-string-index-out-of-range/","created":"2025-07-13T15:25:00.945+08:00"}
---

Author: [University of Helsinki](https://programming-23.mooc.fi/)
Type: Website
Topics: #python #mooc #strings
Link: [Python Programming MOOC 2023](https://programming-23.mooc.fi/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
# IndexError: string index out of range

--- 
## Handling String Indexing Errors

When accessing characters in strings using indexing, you may encounter the error message "IndexError: string index out of range" if you try to access an index that doesn't exist in the string.

For example:
```python
input_string = input("Please type in a string: ")
print("The tenth character: " + input_string[9])  # Works fine
print("The eleventh character: " + input_string[10])  # IndexError
```

Similarly, attempting to access the last character using `len(input_string)` as an index will cause an error, as indexing starts from zero.
```python
input_string = input("Please type in a string: ")
print("Last character: " + input_string[len(input_string)])  # IndexError
```

To handle potential errors caused by input, you can add checks in your code. For instance, to avoid errors when attempting to access the first character of an empty input:
```python
input_string = input("Please type in a string: ")
if len(input_string) > 0:
    print("First character: " + input_string[0])
else:
    print("The input string is empty. There is no first character.")
```

By including these checks, you can handle errors gracefully and improve the robustness of your code.
