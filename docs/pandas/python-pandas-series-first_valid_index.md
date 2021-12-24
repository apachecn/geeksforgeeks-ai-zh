# Python | Pandas series . first _ valid _ index()

> 原文:[https://www . geesforgeks . org/python-pandas-series-first _ valid _ index/](https://www.geeksforgeeks.org/python-pandas-series-first_valid_index/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.first_valid_index()**`函数返回给定序列对象中第一个非 NA/null 值的索引。

> **语法:** Series.first_valid_index()
> 
> **参数:**无
> 
> **返回:**标量:索引类型

**示例#1:** 使用`Series.first_valid_index()`函数查找给定序列对象中的第一个有效索引。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([None, 25, 3, 25, 24, 6])

# Create the Index
index_ = ['Coca Cola', 'Sprite', 'Coke', 'Fanta', 'Dew', 'ThumbsUp']

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**
![](img/bf28f0b4b55e8598b4c45e9bda0ed366.png)

现在我们将使用`Series.first_valid_index()`函数来查找给定序列对象中的第一个有效索引。

```py
# return the first valid index
result = sr.first_valid_index()

# Print the result
print(result)
```

**输出:**

![](img/d5a39afed83fc142a8fbcea3cfc1637e.png)
正如我们在输出中看到的，`Series.first_valid_index()`函数已经成功返回了给定序列对象的第一个有效索引。

**示例 2 :** 使用`Series.first_valid_index()`函数查找给定序列对象中的第一个有效索引。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([None, None, None, 18, 65, None, 32, 10, 5, 24, None])

# Create the Index
index_ = pd.date_range('2010-10-09', periods = 11, freq ='M')

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**
![](img/7268fc6125fe2216fb9d51e7fd7e56fa.png)

现在我们将使用`Series.first_valid_index()`函数来查找给定序列对象中的第一个有效索引。

```py
# return the first valid index
result = sr.first_valid_index()

# Print the result
print(result)
```

**输出:**
![](img/deecea890ef177109e66a11ea171dd63.png)
正如我们在输出中看到的，`Series.first_valid_index()`函数已经成功返回了给定序列对象的第一个有效索引。