# 蟒蛇|熊猫系列. as_blocks()

> 原文:[https://www . geesforgeks . org/python-pandas-series-as _ blocks/](https://www.geeksforgeeks.org/python-pandas-series-as_blocks/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.as_blocks()**`函数用于将帧转换为一组数据类型- >构造函数类型，每个类型都有一个同类数据类型。

> **语法:** Series.as_blocks(copy=True)
> 
> **参数:**
> **副本:**布尔型，默认真
> 
> **返回:**值:一组数据类型- >构造函数类型

**示例#1:** 使用`Series.as_blocks()`函数将给定的序列对象作为字典返回。

```py
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

```py
City 1    New York
City 2     Chicago
City 3     Toronto
City 4      Lisbon
City 5         Rio
dtype: object
```

现在我们将使用`Series.as_blocks()`函数返回给定的序列对象作为字典。

```py
# return a dictionary
result = sr.as_blocks()

# Print the result
print(result)
```

**输出:**

```py
{'object': City 1    New York
City 2     Chicago
City 3     Toronto
City 4      Lisbon
City 5         Rio
dtype: object}
```

正如我们在输出中看到的，`Series.as_blocks()`函数已经成功地将给定的序列对象作为字典返回。

**例 2 :** 使用`Series.as_blocks()`函数返回给定的序列对象作为字典。

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

现在我们将使用`Series.as_blocks()`函数返回给定的序列对象作为字典。

```py
# return a dictionary
result = sr.as_blocks()

# Print the result
print(result)
```

**输出:**

```py
{'float64': 2010-12-31 08:45:00    11.0
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
Freq: A-DEC, dtype: float64}
```

正如我们在输出中看到的，`Series.as_blocks()`函数已经成功地将给定的序列对象作为字典返回。