---
part: "4.2"
topic: lists
dg-publish: true
---
Author: [University of Helsinki](https://programming-23.mooc.fi/)
Type: Website
Topics: #python #mooc #list  #introduction
Link: [Python Programming MOOC 2023](https://programming-23.mooc.fi/)
∗:[[00 PROGRAMMING/Python/_Python/Python\|00 PROGRAMMING/Python/_Python/Python]] 

---
## Adding to a specific location
If you want to specify a location in the list where an item should be added, you can use the `insert` method. 
The method adds an item at the specified index. All the items already in the list with an index equal to or higher than the specified index are moved one index further, "to the right":

![Pasted image 20230812164432.png](/img/user/PROGRAMMING/Python/0%20Python%20Programming%20MOOC/Introduction/Part%204/02%20Lists/attachments/Pasted%20image%2020230812164432.png)

```python
numbers = [1, 2, 3, 4, 5, 6]
numbers.insert(0, 10)
print(numbers)
numbers.insert(2, 20)
print(numbers)
```

