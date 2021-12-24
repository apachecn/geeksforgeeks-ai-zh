# 蟒蛇|熊猫系列. to_dict()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-to_dict/](https://www.geeksforgeeks.org/python-pandas-series-to_dict/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

Pandas `**Series.to_dict()**`函数用于将给定的 Series 对象转换为{label - > value} dict 或 dict 样对象。

> **语法:** Series.to_dict(into=)
> 
> **参数:**
> **进入:**收藏。映射子类以用作返回对象。
> 
> **返回:** value_dict : collections。绘图

**示例#1:** 使用`Series.to_dict()`函数将给定的序列对象转换为字典。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['New York', 'Chicago', 'Toronto', 'Lisbon', 'Rio', 'Moscow'])

# Create the Datetime Index
didx = pd.DatetimeIndex(start ='2014-08-01 10:00', freq ='W', 
                     periods = 6, tz = 'Europe/Berlin') 

# set the index
sr.index = didx

# Print the series
print(sr)
```

**输出:**

![](img/b50676c0b2fee5f5081a878b2e8c0c96.png)

现在我们使用`Series.to_dict()`函数将给定的序列对象转换成字典。

```py
# convert to dictionary
sr.to_dict()
```

**输出:**

![](img/b40643b8810eafb7505af01f8ad96614.png)
正如我们在输出中看到的，`Series.to_dict()`函数已经成功地将给定的序列对象转换为字典。

**示例 2:** 使用`Series.to_dict()`功能将给定的序列对象转换为字典。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([19.5, 16.8, 22.78, 20.124, 18.1002])

# Print the series
print(sr)
```

**输出:**

![](img/a3a0b30092578b29f9be598ce37cd26d.png)

现在我们使用`Series.to_dict()`函数将给定的序列对象转换成字典。

```py
# convert to dictionary
sr.to_dict()
```

**输出:**

![](img/bcf00dfcfab504673cdadb74b620847d.png)

正如我们在输出中看到的，`Series.to_dict()`函数已经成功地将给定的序列对象转换为字典。