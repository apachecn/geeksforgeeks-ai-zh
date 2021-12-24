# Python | Pandas series . aggregate()

> 原文:[https://www . geesforgeks . org/python-pandas-series-aggregate/](https://www.geeksforgeeks.org/python-pandas-series-aggregate/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

Pandas `**Series.aggregate()**`函数在给定系列对象的指定轴上使用一个或多个操作进行聚合。

> **语法:** Series.aggregate(func，axis=0，*args，* * * kwargs)
> 
> **参数:**
> **功能:**功能用于汇总数据。
> **轴:**与数据框兼容所需的参数。
> ***参数:**要传递给 func 的位置参数。
> ****kwargs :** 要传递给 func 的关键字参数。
> 
> **返回:**数据帧、序列或标量

**示例#1:** 使用`Series.aggregate()`函数对给定序列对象的底层数据进行聚合。

```py
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

```py
Coca Cola    34
Sprite        5
Coke         13
Fanta        32
Dew           4
ThumbsUp     15
dtype: int64
```

现在我们使用`Series.aggregate()`函数来求给定数列对象中所有值的和。

```py
# Find the sum of all values
result = sr.aggregate(func = sum)

# Print the result
print(result)
```

**输出:**

```py
103
```

正如我们在输出中看到的，`Series.aggregate()`函数已经成功地返回了给定序列对象的底层数据之和。

**例 2 :** 使用`Series.aggregate()`函数对给定序列对象的底层数据进行聚合。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([51, 10, 24, 18, 1, 84, 12, 10, 5, 24, 0])

# Create the Index
# apply yearly frequency
index_ = pd.date_range('2010-10-09 08:45', periods = 11, freq ='Y')

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**

```py
2010-12-31 08:45:00    51
2011-12-31 08:45:00    10
2012-12-31 08:45:00    24
2013-12-31 08:45:00    18
2014-12-31 08:45:00     1
2015-12-31 08:45:00    84
2016-12-31 08:45:00    12
2017-12-31 08:45:00    10
2018-12-31 08:45:00     5
2019-12-31 08:45:00    24
2020-12-31 08:45:00     0
Freq: A-DEC, dtype: int64
```

现在我们将使用`Series.aggregate()`函数来寻找给定序列对象中所有值的最大值。

```py
# Find the max of all values
result = sr.aggregate(func = max)

# Print the result
print(result)
```

**输出:**

```py
84
```

正如我们在输出中看到的那样，`Series.aggregate()`函数已经成功地返回了给定序列对象中所有值的最大值。