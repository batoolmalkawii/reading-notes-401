# Explore the Tech! 

## _Pandas_ in Python:

#### Importing:
```
In [1]: import numpy as np

In [2]: import pandas as pd
```

#### Object Creation:
* Creating a Series by passing a list of values, letting pandas create a default integer index:
```
In [3]: s = pd.Series([1, 3, 5, np.nan, 6, 8])
```

* Creating a DataFrame by passing a NumPy array, with a datetime index and labeled columns:
```
In [5]: dates = pd.date_range('20130101', periods=6)
```

* Creating a DataFrame by passing a dict of objects that can be converted to series-like.
```
In [9]: df2 = pd.DataFrame({'A': 1.,
   ...:                     'B': pd.Timestamp('20130102'),
   ...:                     'C': pd.Series(1, index=list(range(4)), dtype='float32'),
   ...:                     'D': np.array([3] * 4, dtype='int32'),
   ...:                     'E': pd.Categorical(["test", "train", "test", "train"]),
   ...:                     'F': 'foo'})
   ...: 
```

#### Viewing Data:
Here is how to view the top and bottom rows of the frame:
```
In [13]: df.head()
Out[13]: 
                   A         B         C         D
2013-01-01  0.469112 -0.282863 -1.509059 -1.135632
2013-01-02  1.212112 -0.173215  0.119209 -1.044236
2013-01-03 -0.861849 -2.104569 -0.494929  1.071804
2013-01-04  0.721555 -0.706771 -1.039575  0.271860
2013-01-05 -0.424972  0.567020  0.276232 -1.087401
```

> DataFrame.to_numpy() gives a NumPy representation of the underlying data.
Note that this can be an expensive operation when your DataFrame has columns with different data types,
which comes down to a fundamental difference between pandas and NumPy:
NumPy arrays have one dtype for the entire array, 
while pandas DataFrames have one dtype per column. When you call DataFrame.to_numpy(), 
pandas will find the NumPy dtype that can hold all of the dtypes in the DataFrame. 
This may end up being object, which requires casting every value to a Python object.
>


#### Getting
* Selecting a single column, which yields a Series, equivalent to df.A:
```
In [23]: df['A']
```

* Selecting via [], which slices the rows.
```
In [24]: df[0:3]
```
* Selection by label.
* Selection by position.

#### Setting:
Setting a new column automatically aligns the data by the indexes.
```
In [45]: s1 = pd.Series([1, 2, 3, 4, 5, 6], index=pd.date_range('20130102', periods=6))
```

#### Missing data:
pandas primarily uses the value np.nan to represent missing data. It is by default not included in computations. See the Missing Data section.

Reindexing allows you to change/add/delete the index on a specified axis. This returns a copy of the data.
```
In [55]: df1 = df.reindex(index=dates[0:4], columns=list(df.columns) + ['E'])
```
