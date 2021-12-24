# 蟒蛇|熊猫系列. count()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-count/](https://www.geeksforgeeks.org/python-pandas-series-count/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.count()**`函数返回给定系列对象中`non-NA/null`观察的计数。

> **语法:**系列.计数(级别=无)
> 
> **参数:**
> **级别:**如果轴是多索引(分层的)，则沿着特定级别计数，折叠成较小的系列
> 
> **返回:** nobs : int 或 Series(如果指定了级别)

**示例#1:** 使用`Series.count()`函数查找给定序列对象中非缺失值的计数。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([80, 25, 3, 25, 24, 6])

# Create the Index
index_ = ['Coca Cola', 'Sprite', 'Coke', 'Fanta', 'Dew', 'ThumbsUp']

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**
![](img/106ef1493646a7192f479e267f23abf9.png)

现在我们将使用`Series.count()`函数来查找给定序列对象中非缺失值的计数。

```py
# find the count of non-missing values
# in the given series object
result = sr.count()

# Print the result
print(result)
```

**输出:**
![](img/515e4ccde6fa2d0e58e36f46b1611a09.png)
正如我们在输出中看到的，`Series.count()`函数已经成功地返回了给定序列对象中非缺失值的计数。

**示例 2 :** 使用`Series.count()`函数查找给定序列对象中非缺失值的计数。给定的序列对象包含一些缺失的值。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([100, None, None, 18, 65, None, 32, 10, 5, 24, None])

# Create the Index
index_ = pd.date_range('2010-10-09', periods = 11, freq ='M')

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**
![](img/dd577410a226791fba292b627d327786.png)

现在我们将使用`Series.count()`函数来查找给定序列对象中非缺失值的计数。

```py
# find the count of non-missing values
# in the given series object
result = sr.count()

# Print the result
print(result)
```

**输出:**
![](img/f0c85c16e9786503d4f4b31489a724c6.png)
正如我们在输出中看到的，`Series.count()`函数已经成功地返回了给定序列对象中非缺失值的计数。