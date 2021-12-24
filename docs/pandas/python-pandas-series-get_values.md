# Python | Pandas series . get _ values()

> 原文:[https://www . geesforgeks . org/python-pandas-series-get _ values/](https://www.geeksforgeeks.org/python-pandas-series-get_values/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.get_values()**`函数返回一个包含给定序列对象的底层数据的数组。

> **语法:** Series.get_values()
> 
> **参数:**无
> 
> **返回:**正常

**示例#1:** 使用`Series.get_values()`函数返回包含给定序列对象的基础数据的数组。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([10, 25, 3, 25, 24, 6])

# Create the Index
index_ = ['Coca Cola', 'Sprite', 'Coke', 'Fanta', 'Dew', 'ThumbsUp']

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**
![](img/1f53af828e1a9600b255c9201272ff8a.png)

现在我们将使用`Series.get_values()`函数以数组的形式返回给定序列对象的底层数据。

```py
# return an array
result = sr.get_values()

# Print the result
print(result)
```

**输出:**

![](img/651c65f67a7bedd600915794cdcdc17e.png)
正如我们在输出中看到的，`Series.get_values()`函数已经将给定的序列对象作为数组返回。

**示例 2 :** 使用`Series.get_values()`函数返回包含给定序列对象的底层数据的数组。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([11, 21, 8, 18, 65, 84, 32, 10, 5, 24, 32])

# Create the Index
index_ = pd.date_range('2010-10-09', periods = 11, freq ='M')

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**

![](img/229bdc336ad3db176b98acf5dad7297f.png)

现在我们将使用`Series.get_values()`函数以数组的形式返回给定序列对象的底层数据。

```py
# return an array
result = sr.get_values()

# Print the result
print(result)
```

**输出:**
![](img/40b7aff9eeafeaec071ffec9f40f497e.png)
正如我们在输出中看到的，`Series.get_values()`函数已经将给定的序列对象作为数组返回。