# Python | Pandas series . add _ 后缀()

> 原文:[https://www . geesforgeks . org/python-pandas-series-add _ 后缀/](https://www.geeksforgeeks.org/python-pandas-series-add_suffix/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

Pandas `**Series.add_suffix()**`功能用于在给定系列对象的索引标签末尾添加后缀。

> **语法:**series . add _ 后缀(后缀)
> 
> **参数:**
> **后缀:**每个标签后要添加的字符串。
> 
> **返回:**序列或数据帧

**示例#1:** 使用`Series.add_suffix()`函数在给定序列对象中的每个索引标签的末尾添加后缀。

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

现在我们将使用`Series.add_suffix()`函数在给定序列对象中的每个索引标签的末尾添加后缀“_IPL 2019”。

```
# add '_IPL 2019' to each index labels
result = sr.add_suffix(suffix = '_IPL 2019')

# Print the result
print(result)
```

**输出:**

```
Coca Cola_IPL 2019    34
Sprite_IPL 2019        5
Coke_IPL 2019         13
Fanta_IPL 2019        32
Dew_IPL 2019           4
ThumbsUp_IPL 2019     15
dtype: int64
```

正如我们在输出中看到的那样，`Series.add_suffix()`函数已经成功地在给定序列对象中的每个索引标签的末尾添加了传递的后缀。

**示例 2 :** 使用`Series.add_suffix()`函数在给定系列对象中的每个索引标签的末尾添加后缀。

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

现在我们将使用`Series.add_suffix()`函数在给定序列对象中的每个索引标签的末尾添加后缀“_Date”。

```
# add '_Date' to each index labels
result = sr.add_suffix(suffix = '_Date')

# Print the result
print(result)
```

**输出:**

```
2010-12-31 08:45:00_Date    51
2011-12-31 08:45:00_Date    10
2012-12-31 08:45:00_Date    24
2013-12-31 08:45:00_Date    18
2014-12-31 08:45:00_Date     1
2015-12-31 08:45:00_Date    84
2016-12-31 08:45:00_Date    12
2017-12-31 08:45:00_Date    10
2018-12-31 08:45:00_Date     5
2019-12-31 08:45:00_Date    24
2020-12-31 08:45:00_Date     0
dtype: int64
```

正如我们在输出中看到的那样，`Series.add_suffix()`函数已经成功地在给定序列对象中的每个索引标签的末尾添加了传递的后缀。