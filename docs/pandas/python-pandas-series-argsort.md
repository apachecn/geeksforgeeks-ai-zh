# Python |熊猫系列. argsort()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-argsort/](https://www.geeksforgeeks.org/python-pandas-series-argsort/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.argsort()**`函数返回给定序列对象的基础数据排序的索引。

> **语法:** Series.argsort(axis=0，kind='quicksort '，order=None)
> 
> **参数:**
> **轴:**无效果但兼容 numpy 接受。
> **种类:** {'mergesort '，' quicksort '，' heapsort'}，默认' quicksort'
> **顺序:**无影响但接受与 numpy 兼容。
> 
> **返回:** argsorted : Series，其中-1 表示存在 nan 值的位置

**示例#1:** 使用`Series.argsort()`函数返回索引序列，该序列将对给定序列对象的底层数据进行排序。

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

现在我们将使用`Series.argsort()`函数返回一个索引序列，该序列将对给定序列对象的底层数据进行排序。

```py
# return the indices which will
# sort the series
result = sr.argsort()

# Print the result
print(result)

# Let's sort the series using the result
print(sr[result])
```

**输出:**

```py
Coca Cola    4
Sprite       1
Coke         2
Fanta        5
Dew          3
ThumbsUp     0
dtype: int64

Dew           4
Sprite        5
Coke         13
ThumbsUp     15
Fanta        32
Coca Cola    34
dtype: int64
```

正如我们在输出中看到的那样，`Series.argsort()`函数已经成功地返回了一个包含索引的序列对象，这些索引将对给定的序列对象进行排序。

**示例 2 :** 使用`Series.argsort()`函数返回索引序列，该序列将对给定序列对象的底层数据进行排序。

```py
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

```py
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

现在我们将使用`Series.argsort()`函数返回一个索引序列，该序列将对给定序列对象的底层数据进行排序。

```py
# return the indices which will
# sort the series
result = sr.argsort()

# Print the result
print(result)

# Let's sort the series using the result
print(sr[result])
```

**输出:**

```py
2010-12-31 08:45:00    8
2011-12-31 08:45:00    2
2012-12-31 08:45:00    7
2013-12-31 08:45:00    0
2014-12-31 08:45:00    3
2015-12-31 08:45:00    5
2016-12-31 08:45:00    1
2017-12-31 08:45:00    6
2018-12-31 08:45:00    9
2019-12-31 08:45:00    4
2020-12-31 08:45:00   -1
Freq: A-DEC, dtype: int64

2018-12-31 08:45:00     5.0
2012-12-31 08:45:00     8.0
2017-12-31 08:45:00    10.0
2010-12-31 08:45:00    11.0
2013-12-31 08:45:00    18.0
2015-12-31 08:45:00    18.0
2011-12-31 08:45:00    21.0
2016-12-31 08:45:00    32.0
2019-12-31 08:45:00    32.0
2014-12-31 08:45:00    65.0
2020-12-31 08:45:00     NaN
dtype: float64
```

正如我们在输出中看到的那样，`Series.argsort()`函数已经成功地返回了一个包含索引的序列对象，这些索引将对给定的序列对象进行排序。请注意，函数返回了-1 作为缺失值的索引位置。