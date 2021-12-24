# 蟒蛇|熊猫系列. all()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-all/](https://www.geeksforgeeks.org/python-pandas-series-all/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.all()**`函数返回所有元素是否为真，可能在一个轴上。它返回`True`，除非在一个序列中或沿着数据框轴至少有一个元素是`False`或等效的(例如零或空)。

> **语法:** Series.all(axis=0，bool_only=None，skipna=True，level=None，**kwargs)
> 
> **参数:**
> **轴:**表示应该减少哪个轴或哪些轴。
> **仅布尔:**仅包含布尔列。
> **skipna :** 排除 NA/null 值。
> **级别:**如果轴是一个多索引(分层)，沿着特定级别计数，折叠成一个标量。
> ****kwargs :** 附加关键字没有影响，但可能会被接受以与 NumPy 兼容。
> 
> **返回:**标量或级数

**示例#1:** 使用`Series.all()`功能检查给定序列对象中的所有值是真还是非零。

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

现在我们将使用`Series.all()`函数检查给定序列对象中的所有值是否为真非零。

```
# check if all value is True
# or non-zero
result = sr.all()

# Print the result
print(result)
```

**输出:**

```
True
```

正如我们在输出中看到的那样，`Series.all()`函数已经成功返回了`True`，表明给定序列中的所有值都为真或非零。

**示例 2 :** 使用`Series.all()`功能检查给定系列对象中的所有值是否为真或非零。

```
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

```
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

现在我们将使用`Series.all()`函数检查给定序列对象中的所有值是否为真非零。

```
# check if all value is True
# or non-zero
result = sr.all()

# Print the result
print(result)
```

**输出:**

```
False
```

从输出中我们可以看到，`Series.all()`函数已经成功返回了`False`，表示给定序列中的所有值都不是真或非零。该系列对象中的一个值为零。