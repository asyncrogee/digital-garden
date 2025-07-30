---
{"dg-publish":true,"permalink":"/notes/data/python-data-fundamentals/pandas/loop-over-data-frame/","tags":["data","python"],"created":"2025-07-15T21:24:22.399+08:00"}
---

---
> [!abstract] Table of Contents
---

### Loop over DataFrame

Iterating over a  Pandas DataFrame is typically done with the `iterrows()`:
```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Iterate over rows of cars
for lab, row in cars.iterrows():
    print(lab)
    print(row)
```

Adding a New Column:
```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Code for loop that adds COUNTRY column
for lab, row in cars.iterrows():
    cars.loc[lab, "COUNTRY"] = row["country"].upper()

# Print cars
print(cars)
```

Adding a New Column using `apply()`:
```python
for lab, row in brics.iterrows() :
    brics.loc[lab, "name_length"] = len(row["country"])
    
# SAME RESULT AS:
brics["name_length"] = brics["country"].apply(len)
```

```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Use .apply(str.upper)

cars["COUNTRY"] = cars["country"].apply(str.upper)

print(cars)
```