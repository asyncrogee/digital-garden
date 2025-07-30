---
{"dg-publish":true,"permalink":"/notes/data/python-data-fundamentals/matplotlib/matplotlib/","tags":["data","python"],"created":"2025-07-13T15:25:33.920+08:00"}
---

---
> [!abstract] Table of Contents
> - [[#Basic Plots]]
> 	- [[#`Matplotlib.pyplot` Functions]]
> - [[#Histogram]]
> - [[#Plot Customization]]
> 	- [[#Example customization of plot]]
> 	- [[#Scatter Plot Customization]]


> [!info]- Matplotlib
> ##### Data visualization
> ![Pasted image 20250610093928.png](/img/user/Misc/attachments/Pasted%20image%2020250610093928.png)
> ###### Example plot:
> ![Pasted image 20250610094122.png](/img/user/Misc/attachments/Pasted%20image%2020250610094122.png)

> [!abstract] Functions
> ##### Visualize
> -  `.plot(x_data, y_data)`: or __Line Plot__ Tells python ___what to plot and how to plot_ __ 
> - `.scatter(x_data, y_data)`: or __Scatter Plot__ same as `.plot()` but ___DOTTED___
> - `.hist(data, bins=3)`: Histogram
> - `plt.show()`: __Displays__ the plot
> - `plt.clf()` clear previous plot
>   
>  ##### Transform
> - `.xscale('log')`/`.yscale('log')`: Transforms the labels in the x or y-axis into a logarithmic scale
> 	- ![Pasted image 20250610100115.png](/img/user/Misc/attachments/Pasted%20image%2020250610100115.png)

---
## Basic Plots
> [!example]
> ###### Line plot:
> ```python
> import matpltolib.pyplot as plt
> year = [1950, 1970, 1990, 2010]
> pop = [2.519, 3.692, 5.263, 6.972]
> plt.plot(year, pop)
> plt.show()
>```
>![[Pasted image 20250610094535.png]]
>
>###### Scatter plot:
>```python
>import matplotlib.pyplot as plt
> year = [1950, 1970, 1990, 2010]
> pop = [2.519, 3.692, 5.263, 6.972]
> plt.scatter(year, pop)
> plt.show()
>```
>![[Pasted image 20250610094825.png]]

---
## Histogram
- Useful to explore dataset
- Get idea about distribution

![[Pasted image 20250610103219.png]]
- Shows an overview of how values are distributed in each __bins__

```python
hist(x, bins=None)
```
- `x` is the `list/data`
- `bins` is the amount of bins where the data will be divided

> [!example]
> ```python
>import matplotlib.pyplot as plt
>
>values = [0, 0.6, 1.4, 1.6, 2.2, 2.5, 2.6, 3.2, 3.5, 3.9,4.2, 6]
>plt.hist(values, bins=3)
># or
>plt.hist(values, 3)
>plt.show()
> ```
> ![[Pasted image 20250610104128.png]]
> 
> ###### More Example:
> ![[Pasted image 20250610104157.png]]

## Plot Customization
Make sure to call these functions before calling the  `.show()` function for them to show.

##### Example customization of plot:
```python
import matplotlib.pyplot as plt
year = [1950, 1951, 1952, ..., 2100]
pop = [2.538, 2.57, 2.62, ..., 10.85]

# Add more data:
year = [1800, 1850, 1900] + year
pop = [1.0, 1.262, 1.650] + pop

plt.plot(year, pop)

# X-axis Label:
plt.xlabel('Year')

# Y-axis Label:
plt.ylabel('Population')

# Title Label on Top of the Plot
plt.title('World Population Projections')


# Modify the numbers/ticks:
plt.yticks([0, 2, 4, 6, 8, 10],
			['0', '2B', '4B', '6B', '8B', '10B']) # to be clear that it's "B(illions)" we put this 2nd argument of lists
```
Output:
![[Pasted image 20250610135540.png]]
##### Scatter Plot Customization
```python
plt.scatter(x = gdp_cap, y = life_exp, s = np.array(pop) * 2, c = col, alpha = 0.8)
```
- `c = col` is the colors
```python
dict = {
    'Asia':'red',
    'Europe':'green',
    'Africa':'blue',
    'Americas':'yellow',
    'Oceania':'black'
}
```
- `alpha = 0.8` is the opacity of the bubbles, can be set from `0 to 1`
![[Pasted image 20250610152352.png]]

##### Additional Customization(Grid & Text):
```python
plt.grid(True)

plt.text(1550, 71, 'India')
plt.text(5700, 80, 'China')
```
![[Pasted image 20250610152605.png]]

---
