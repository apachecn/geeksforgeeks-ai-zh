# 蟒蛇|熊猫系列. max()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-max/](https://www.geeksforgeeks.org/python-pandas-series-max/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.max()**`函数返回给定序列对象中底层数据的最大值。即使只返回一个值，该函数也总是返回 Series。

> **语法:**series . max(axis =无，skipna =无，level =无，numeric _ only =无，**kwargs)
> 
> **参数:**
> **轴:**轴为要应用的功能。
> **skipna :** 计算结果时排除 NA/null 值。
> **级别:**如果轴是多索引(分层)，则沿着特定级别计数，折叠成标量。
> **numeric_only :** 只包括 float、int、boolean 列。
> ****kwargs :** 要传递给函数的附加关键字参数。
> 
> **返回:**最大值:标量或级数(如果指定了级别)

**示例#1:** 使用`Series.max()`函数在给定序列对象的底层数据中找到最大值。

```
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

现在我们用`Series.max()`函数求给定数列对象的最大值。

```
# return the maximum value in the 
# series object
result = sr.max()

# Print the result
print(result)
```

**输出:**
![](img/194181082d65a4de8d585f6816a1da95.png)
我们可以在输出中看到，`Series.max()`函数已经成功返回给定序列对象的最大值。

**例 2:** 使用`Series.max()`函数在给定序列对象的底层数据中寻找最大值。给定的序列对象也包含一些缺失的值。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([19.5, 16.8, None, 22.78, 16.8, 20.124, None, 18.1002, 19.5])

# Print the series
print(sr)
```

**输出:**

![](img/6b220f17b68c4b02f78f526bdf6df4a0.png)

现在我们用`Series.max()`函数求给定数列对象的最大值。我们将跳过丢失的值，同时找到最大值。

```
# return the maximum value in the series object
# skip the missing values
result = sr.max(skipna = True)

# Print the result
print(result)
```

**输出:**
![](img/d68541fb832ac0826f9fbf03794cdd6a.png)
在输出中我们可以看到，`Series.max()`函数已经成功返回了给定序列对象的最大值。