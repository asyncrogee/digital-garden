---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/python/0-python-programming-mooc/introduction/part-3/03-more-loops/02-continue-command/","created":"2025-07-13T15:25:00.981+08:00"}
---

Author: [University of Helsinki](https://programming-23.mooc.fi/)
Type: Website
Topics: #python #mooc #commands #loops 
Link: [Python Programming MOOC 2023](https://programming-23.mooc.fi/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
# 02 Continue command

--- 
## Using the `continue` Command in Loops

The `continue` command is used to skip the rest of the current iteration and move directly to the next iteration of the loop. It effectively jumps back to the beginning of the loop and reevaluates the loop's condition.
![[Pasted image 20230828200556.png]]

Example: Summing numbers smaller than 10 using `continue`:
```python
sum = 0

while True:
    number = int(input("Please type in a number, -1 to exit: "))
    if number == -1:
        break
    if number >= 10:
        continue
    sum += number

print(f"The sum is {sum}")
```

In this example, if the input number is greater than or equal to 10, the `continue` command is executed, skipping the addition of that number to the sum and jumping directly to the next iteration of the loop.

The output of the program shows the sum of only those numbers that are less than 10.
