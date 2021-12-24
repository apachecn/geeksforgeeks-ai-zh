# 蟒蛇|熊猫系列. to_frame()

> 原文:[https://www . geesforgeks . org/python-pandas-series-to _ frame/](https://www.geeksforgeeks.org/python-pandas-series-to_frame/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.to_frame()**`功能用于将给定的序列对象转换为数据帧。

> **语法:** Series.to_frame(名称=无)
> 
> **参数:**
> **名称:**传递的名称应该替换系列名称(如果有)。
> 
> **返回:**数据帧:数据帧

**示例#1:** 使用`Series.to_frame()`函数将给定的序列对象转换为数据帧。

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

现在我们将使用`Series.to_frame()`函数将给定的序列对象转换为数据帧。

```py
# convert to dataframe
sr.to_frame()
```

**输出:**

![](img/fda7071330ee3486e1804cc5f4a14377.png)

正如我们在输出中看到的那样，`Series.to_frame()`函数已经成功地将给定的序列对象转换为数据帧。

**示例#2:** 使用`Series.to_frame()`函数将给定的序列对象转换为数据帧。

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

现在我们将使用`Series.to_frame()`函数将给定的序列对象转换为数据帧。

```py
# convert to dataframe
sr.to_frame()
```

**输出:**

![](img/406fd6e64418aba865eceee6c467eefe.png)

正如我们在输出中看到的那样，`Series.to_frame()`函数已经成功地将给定的序列对象转换为数据帧。