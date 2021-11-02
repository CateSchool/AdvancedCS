# Data

Installing Jupyter
How to use Jupyter Notebooks
NumPy and Pandas introduction

NumPy array (ndarray): 
* Better than Python list b/c you can do more operations more easily

Pandas Series
* like NumPy array but with named indices, rather than just numbers 0, 1, 2, ...

Pandas DataFrame
* similar to a matrix
* a column of a DataFrame is basically a Series

```python
df = pd.read_csv('shoefly_orders.csv')
df.head(10)
```


pandas:
In this documentation you will learn about Pandas, a python library for data analysis. This library is helpful if you would like to perform data manipulation (slicing, dicing, joining, merging, grouping) and analysis.