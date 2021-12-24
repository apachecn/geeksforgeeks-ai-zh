# 蟒蛇|熊猫系列. rmod()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-rmod/](https://www.geeksforgeeks.org/python-pandas-series-rmod/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.rmod()**`函数执行序列和其他元素的模运算(二进制运算符 rmul)。该操作等同于其他%系列，但支持用 fill_value 替换其中一个输入中缺失的数据。

> **语法:** Series.rmod(其他，级别=无，fill _ value =无，轴=0)
> 
> **参数:**
> **其他:**系列或标量值
> **填充 _ 值:**填充现有缺失(NaN)值
> **等级:**跨一级广播，
> 
> **返回:**结果:系列

**示例#1:** 使用`Series.rmod()`函数对给定的序列对象执行标量模运算。

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
现在我们使用`Series.rmod()`函数对级数进行标量模运算。

```py
# find modulo of the given value with series
result = sr.rmod(2000)

# Print the result
print(result)
```

**输出:**

![](img/502f63e3bbb99c8c1ac2fb09dad1885b.png)
正如我们在输出中看到的，`Series.rmod()`函数返回了给定标量与级数对象的模运算结果。

**示例#2:** 使用`Series.rmod()`函数对给定的序列对象执行标量模运算。给定的序列对象包含一些缺失的值。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([19.5, 16.8, None, 22.78, None, 20.124, None, 18.1002, None])

# Print the series
print(sr)
```

**输出:**

![](img/c138b3dfc592caf9841b8cf3acb6efb0.png)

现在我们将使用`Series.rmod()`函数对级数进行标量模运算。我们还将在缺少值的地方填充 10。

```py
# find modulo of the given value with series
# fill 10 at the place of missing values
result = sr.rmod(2000, fill_value = 10)

# Print the result
print(result)
```

**输出:**

![](img/1f6eafe1f59437b35f0089eb6ac7f4de.png)

正如我们在输出中看到的，`Series.rmod()`函数返回了给定标量与级数对象的模运算结果。