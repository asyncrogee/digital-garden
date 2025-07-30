---
{"dg-publish":true,"permalink":"/notes/data/python-data-fundamentals/num-py/num-py/","tags":["data","python"],"created":"2025-07-13T15:25:33.918+08:00"}
---

---
> [!abstract] Table of Contents

---
> [!warning]
> Boolean Operators (OR, AND, etc.) will not work with NumPy
> ```python
> import numpy as np
> my_house = np.array([18.0, 20.0, 10.75, 9.50])
> your_house  = np.array([14.0, 24.0, 14.25, 9.0])
> 
> # THIS WILL NOT WORK:
> my_house > 18.5 or your_house < 10
> 
> ```

Instead...

> [!info] We could use these:
> - `np.logical_or()`
> - `np.logical_not()`
> - `np.logical_and()`

> [!example] Boolean Operators with NumPy
> ```python
> import numpy as np
> my_house = np.array([18.0, 20.0, 10.75, 9.50])
> your_house  = np.array([14.0, 24.0, 14.25, 9.0])
> 
> # THIS WOULD WORK WITH NUMPY:
> np.logical_or(my_house > 18.5, my_house < 10)
> np.logical_and(my_house < 11, your_house < 11)
> ```
