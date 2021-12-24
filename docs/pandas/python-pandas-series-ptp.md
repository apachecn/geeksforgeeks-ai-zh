# 蟒蛇|熊猫系列. ptp()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-ptp/](https://www.geeksforgeeks.org/python-pandas-series-ptp/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.ptp()**`函数返回对象中最大值和
最小值之间的差值。这相当于`numpy.ndarray`法`ptp`。

> **语法:**series . PTP(axis =无，skipna =无，level =无，numeric _ only =无，**kwargs)
> 
> **参数:**
> **轴:**轴为要应用的功能。
> **skipna :** 计算结果时排除 NA/null 值。
> **级别:**如果轴是多索引(分层)，则沿着特定级别计数，折叠成标量。
> **numeric_only :** 只包括 float、int、boolean 列。如果没有，将尝试使用所有内容，然后只使用数字数据。不适用于系列。
> ****kwargs :** 要传递给函数的附加关键字参数。
> 
> **返回:** ptp:标量或序列(如果指定了级别)

**示例#1:** 使用`Series.ptp()`函数返回给定 Series 对象中基础数据的最大值和最小值之间的差值。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([10, 25, 3, 11, 24, 6])

# Create the Index
index_ = ['Coca Cola', 'Sprite', 'Coke', 'Fanta', 'Dew', 'ThumbsUp']

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**

![](img/dab04769c1239f7411b50876f1fa5e58.png)

现在我们将使用`Series.ptp()`函数来查找给定序列对象中最大值和最小值之间的差异。

```py
# return the difference between the 
# maximum and the minimum value
result = sr.ptp()

# Print the result
print(result)
```

**输出:**

![](img/79afa2841a44a6eea8b2ff813154d9f5.png)

从输出中我们可以看到，`Series.ptp()`函数已经成功地返回了给定序列对象中底层数据的最大值和最小值之间的差值。

**示例#2:** 使用`Series.ptp()`函数返回给定 Series 对象中基础数据的最大值和最小值之间的差值。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([11, 21, 8, 18, 65, 84, 32, 10, 5, 24, 32])

# Print the series
print(sr)
```

**输出:**

![](img/d52f8833298554c10ba883da368913f5.png)

现在我们将使用`Series.ptp()`函数来查找给定序列对象中最大值和最小值之间的差异。

```py
# return the difference between the 
# maximum and the minimum value
result = sr.ptp()

# Print the result
print(result)
```

**输出:**

![](img/51f33cf08ae7160316253a8fff536695.png)

从输出中我们可以看到，`Series.ptp()`函数已经成功地返回了给定序列对象中底层数据的最大值和最小值之间的差值。

**示例#3:** 使用`Series.ptp()`函数返回给定 Series 对象中基础数据的最大值和最小值之间的差值。给定的序列对象中包含一些缺失的值。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([19.5, 16.8, None, 22.78, None, 20.124, None, 18.1002, None])

# Print the series
print(sr)
```

**输出:**

![](img/f1da4795c32426d8ce1e60f777931fb5.png)

现在我们将使用`Series.ptp()`函数来查找给定序列对象中最大值和最小值之间的差异。我们将跳过计算中缺失的值。

```py
# return the difference between the 
# maximum and the minimum value
result = sr.ptp(skipna = True)

# Print the result
print(result)
```

**输出:**

![](img/2ef0e59440efa51d2dfc4be2fd65a2e0.png)

从输出中我们可以看到，`Series.ptp()`函数已经成功地返回了给定序列对象中底层数据的最大值和最小值之间的差值。