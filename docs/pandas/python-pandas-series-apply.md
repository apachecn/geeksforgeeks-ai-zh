# 蟒蛇|熊猫系列. apply()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-apply/](https://www.geeksforgeeks.org/python-pandas-series-apply/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.apply()**`函数调用给定序列对象的每个元素上传递的函数。

> **语法:** Series.apply(func，convert_dtype=True，args=()，**kwds)
> 
> **参数:**
> **函数:** Python 函数或 NumPy ufunc 来应用。
> **convert_dtype :** 尝试为 elementwise 函数结果找到更好的 dtype。
> **参数:**在序列值之后传递给 func 的位置参数。
> ****kwds :** 传递给 func 的其他关键字参数。
> 
> **返回:**系列

**示例#1:** 如果城市是‘里约’，使用`Series.apply()`功能将城市名称更改为‘蒙特利尔’。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['New York', 'Chicago', 'Toronto', 'Lisbon', 'Rio'])

# Create the Index
index_ = ['City 1', 'City 2', 'City 3', 'City 4', 'City 5'] 

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**

```
City 1    New York
City 2     Chicago
City 3     Toronto
City 4      Lisbon
City 5         Rio
dtype: object
```

现在如果城市是‘里约’，我们将使用`Series.apply()`功能将城市名称更改为‘蒙特利尔’。

```
# change 'Rio' to 'Montreal'
# we have used a lambda function
result = sr.apply(lambda x : 'Montreal' if x =='Rio' else x )

# Print the result
print(result)
```

**输出:**

```
City 1    New York
City 2     Chicago
City 3     Toronto
City 4      Lisbon
City 5    Montreal
dtype: object
```

正如我们在输出中看到的，`Series.apply()`功能已经成功地将城市名称更改为‘蒙特利尔’。

**示例 2 :** 如果给定系列对象中的值大于 30，则使用`Series.apply()`函数返回真，否则返回假。

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

现在，如果给定序列对象中的值大于 30，我们将使用`Series.apply()`函数返回真，否则返回假。

```
# return True if greater than 30
# else return False
result = sr.apply(lambda x : True if x>30 else False)

# Print the result
print(result)
```

**输出:**

```
2010-12-31 08:45:00    False
2011-12-31 08:45:00    False
2012-12-31 08:45:00    False
2013-12-31 08:45:00    False
2014-12-31 08:45:00     True
2015-12-31 08:45:00    False
2016-12-31 08:45:00     True
2017-12-31 08:45:00    False
2018-12-31 08:45:00    False
2019-12-31 08:45:00     True
2020-12-31 08:45:00    False
Freq: A-DEC, dtype: bool
```

正如我们在输出中看到的那样，`Series.apply()`函数已经成功地返回了给定序列对象的 numpy 数组表示。