---
{"dg-publish":true,"permalink":"/notes/data/python-data-fundamentals/pandas/pandas/","tags":["data","python"],"created":"2025-07-13T15:25:33.915+08:00"}
---

---
> [!abstract] Table of Contents
> - Datasets in Python
> - [[#Changing Labels]]
> - [[#Importing CSV as DataFrames]]
> - [[#Index and Select Data in Pandas]]
> - [[#Examples]]
> - 

---

> [!abstract] Pandas
> -  Used instead of 2D NumPy Array because it doesn't support multiple Data Types
> - High level data manipulation tool
> - Built on NumPy
> - created by Wes McKinney

> [!Example] Datasets in Python
> ![Pasted image 20250610162945.png](/img/user/Misc/attachments/Pasted%20image%2020250610162945.png)
> #### Pandas Version:
> ![Pasted image 20250610163001.png](/img/user/Misc/attachments/Pasted%20image%2020250610163001.png)
> 
> ##### DataFrame from Dictionary:
> ![Pasted image 20250610163120.png](/img/user/Misc/attachments/Pasted%20image%2020250610163120.png)
> - keys (column labels)
> - values (data, column by column)
> ```python
> import pandas as pd
> brics = pd.DataFrame(dict)
> brics.index = ["BR", "RU", "IN", "CH", "SA"]
> brics
> ```
>![Pasted image 20250610163245.png](/img/user/Misc/attachments/Pasted%20image%2020250610163245.png)
>
> #### DataFrame from CSV Files:
> ![Pasted image 20250610163826.png](/img/user/Misc/attachments/Pasted%20image%2020250610163826.png)
> ```python
> brics = pd.read_csv("path/to/brics.csv", index_col = 0)
> ```
> ![Pasted image 20250610163920.png](/img/user/Misc/attachments/Pasted%20image%2020250610163920.png)


### Examples:
```python
# Pre-defined lists
names = ['United States', 'Australia', 'Japan', 'India', 'Russia', 'Morocco', 'Egypt']
dr =  [True, False, False, False, True, True, True]
cpc = [809, 731, 588, 18, 200, 70, 45]

# Import pandas as pd
import pandas as pd

# Create dictionary my_dict with three key:value pairs: my_dict
my_dict = {
    'country': names,
    'drives_right':dr,
    'cars_per_cap':cpc,
}

# Build a DataFrame cars from my_dict: cars
cars = pd.DataFrame(my_dict)

# Print cars
print(cars)
```


##### Importing CSV as DataFrames
```python
# Import pandas as pd
import pandas as pd

# Fix import by including index_col
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out cars
print(cars)
```


### Index and Select Data in Pandas

> [!info] __Column Access__ 
> ![[Pasted image 20250610171524.png]]
> ```python
> brics["country"]
>```
>![[Pasted image 20250610171559.png]]
> ```python
> type(bricks["country"]) # pandas.core.series.Series
> ```
> - 1D labelled array
>
>> [!tip] Select Column but keep data in the DataFrame:
>> - Use double brackets `[[]]`
>> ```python
>> brics[["country", "capital"]]
>> ```
>> ![[Pasted image 20250610172002.png]]
>> ```python
>> type(brics[["country"]]) # pandas.core.frame.DataFrame
>> ```

> [!info] __Row__ Access
> ![[Pasted image 20250610172645.png]]
> ```python
> brics[1:4]
> ```
> ![[Pasted image 20250610172704.png]]

> [!tip] Row Access `loc`
> ![[Pasted image 20250610181919.png \| 400]]
> ```python
> brics.loc[["RU"]]
> ```
> ![[Pasted image 20250610181943.png \| 200]]
> - DataFrame
>   
> #### Select Multiple Rows:
> ```python
> brics.loc[["RU", "IN", "CH"]]
> ```
> ![[Pasted image 20250610182143.png \| 200]]
> 
> #### Row & Column loc
> ```python
> brics.loc[["RU", "IN", "CH"], ["country", "capital"]]
> ```
> ![[Pasted image 20250610182153.png \| 200]]
> 
> #### All Rows:
> ```python
> brics.loc[:, ["country", "capital"]]
> ```
> ![[Pasted image 20250610182243.png \| 200]]

> [!tip] Row Access `iloc`
> ```python
> # in loc:
> brics.loc[["RU", "IN", "CH"]]
> brics.loc[["RU", "IN", "CH"], ["country", "capital"]]
> brics.loc[:, ["country", "capital"]]
> 
> # using iloc:
> brics.iloc[[1, 2, 3]]
> brics.iloc[[1, 2, 3], [0, 1]]
> brics.iloc[:, [0, 1]]
> ```




---
### Examples:
```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out country column as Pandas Series
print(cars["country"])

# Print out country column as Pandas DataFrame
print(cars[["country"]])

# Print out DataFrame with country and drives_right columns
print(cars[["country", "drives_right"]])
```

```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out first 3 observations
print(cars[0:3])

# Print out fourth, fifth and sixth observation
print(cars[3:6])
```

```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out observation for Japan
print(cars.loc["JPN"])

# Print out observations for Australia and Egypt
print(cars.loc[["AUS", "EG"]])
```

```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out drives_right value of Morocco
print(cars.loc["MOR", "drives_right"])

# Print sub-DataFrame
print(cars.loc[["RU", "MOR"], ["country", "drives_right"]])
```

```python
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out drives_right column as Series
print(cars.loc[:, "drives_right"])

# Print out drives_right column as DataFrame
print(cars.loc[:, ["drives_right"]])

# Print out cars_per_cap and drives_right as DataFrame
print(cars.loc[:, ["cars_per_cap", "drives_right"]])
```


---

