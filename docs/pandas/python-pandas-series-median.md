# 蟒蛇|熊猫系列.中位数()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-median/](https://www.geeksforgeeks.org/python-pandas-series-median/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.median()**`函数返回给定序列对象中基础数据的中位数。

> **语法:**系列.中位数(轴=无，skipna =无，级别=无，numeric _ only =无，**kwargs)
> 
> **参数:**
> **轴:**轴为要应用的功能。
> **skipna :** 计算结果时排除 NA/null 值。
> **级别:**如果轴是多索引(分层)，则沿着特定级别计数，折叠成标量。
> **numeric_only :** 仅包括 float、int、boolean 列
> ****kwargs :** 要传递给函数的附加关键字参数。
> 
> **返回:**中值:标量或级数(如果指定了级别)

**示例#1:** 使用`Series.median()`函数找到给定序列对象中底层数据的中值。

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
![](img/8fe72b1b35286fd405b16a26124c8342.png)

现在我们用`Series.median()`函数求给定级数对象的中值。

```py
# return the median
result = sr.median()

# Print the result
print(result)
```

**输出:**
![](img/ff40980dd54340b2e21519c327613a11.png)
正如我们在输出中看到的，`Series.median()`函数已经成功返回了给定序列对象的中值。

**例 2:** 使用`Series.median()`函数求给定序列对象中底层数据的中位数。给定的序列对象包含一些缺失的值。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([19.5, 16.8, None, 22.78, 16.8, 20.124, None, 18.1002, 19.5])

# Print the series
print(sr)
```

**输出:**

![](img/6b220f17b68c4b02f78f526bdf6df4a0.png)

现在我们用`Series.median()`函数求给定级数对象的中值。在计算给定序列对象的中值时，我们将跳过缺失的值。

```py
# return the median
result = sr.median(skipna = True)

# Print the result
print(result)
```

**输出:**
![](img/301ae54e844741ce97eb7deeb6e8deba.png)
正如我们在输出中看到的，`Series.median()`函数已经成功返回了给定序列对象的中值。