# 蟒蛇|熊猫系列. argmax()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-argmax/](https://www.geeksforgeeks.org/python-pandas-series-argmax/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

Pandas `**Series.argmax()**`函数返回给定序列对象中最大值的行标签。

> **语法:** Series.argmax(axis=0，skipna=True，*args，**kwargs)
> 
> **参数:**
> **skipna :** 排除 NA/null 值。如果整个系列都是 NA，结果就是 NA。
> **轴:**用于与 DataFrame.idxmax 兼容。冗余用于系列上的应用。
> ***args，**kwargs :** 其他关键字没有影响，但可能会被接受以与 NumPy 兼容。
> 
> **返回:** idxmax:最大值的索引。

**示例#1:** 使用`Series.argmax()`函数返回给定序列对象中最大值的行标签

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([34, 5, 13, 32, 4, 15])

# Create the Index
index_ = ['Coca Cola', 'Sprite', 'Coke', 'Fanta', 'Dew', 'ThumbsUp']

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**

```
Coca Cola    34
Sprite        5
Coke         13
Fanta        32
Dew           4
ThumbsUp     15
dtype: int64
```

现在我们将使用`Series.argmax()`函数返回给定序列对象中最大值的行标签。

```
# return the row label for
# the maximum value
result = sr.argmax()

# Print the result
print(result)
```

**输出:**

```
Coca Cola
```

从输出中我们可以看到，`Series.argmax()`函数已经成功地返回了给定序列对象中最大值的行标签。

**示例 2 :** 使用`Series.argmax()`函数返回给定序列对象中最大值的行标签。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([11, 21, 8, 18, 65, 18, 32, 10, 5, 32, None])

# Create the Index
# apply yearly frequency
index_ = pd.date_range('2010-10-09 08:45', periods = 11, freq ='Y')

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**

```
2010-12-31 08:45:00    11.0
2011-12-31 08:45:00    21.0
2012-12-31 08:45:00     8.0
2013-12-31 08:45:00    18.0
2014-12-31 08:45:00    65.0
2015-12-31 08:45:00    18.0
2016-12-31 08:45:00    32.0
2017-12-31 08:45:00    10.0
2018-12-31 08:45:00     5.0
2019-12-31 08:45:00    32.0
2020-12-31 08:45:00     NaN
Freq: A-DEC, dtype: float64
```

现在我们将使用`Series.argmax()`函数返回给定序列对象中最大值的行标签。

```
# return the row label for
# the maximum value
result = sr.argmax()

# Print the result
print(result)
```

**输出:**

```
2014-12-31 08:45:00
```

从输出中我们可以看到，`Series.argmax()`函数已经成功地返回了给定序列对象中最大值的行标签。