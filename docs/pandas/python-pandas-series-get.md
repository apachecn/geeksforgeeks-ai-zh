# 蟒蛇|熊猫系列. get()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-get/](https://www.geeksforgeeks.org/python-pandas-series-get/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.get()**`函数从给定键(数据框列、面板切片等)的对象中获取项目。).如果未找到，则返回默认值。

> **语法:** Series.get(键，默认=无)
> 
> **参数:**
> **关键:**对象
> 
> **返回:**值:与对象中包含的项目类型相同

**示例#1:** 使用`Series.get()`函数获取给定序列对象中传递的索引标签的值。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['New York', 'Chicago', 'Toronto', None, 'Rio'])

# Create the Index
index_ = ['City 1', 'City 2', 'City 3', 'City 4', 'City 5'] 

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**
![](img/6a30eac27fdf7531f13988ddcf13d3f4.png)
现在我们将使用`Series.get()`函数返回给定序列对象中传递的索引标签的值。

```py
# return the value corresponding to
# the passe index label
result = sr.get(key = 'City 3')

# Print the result
print(result)
```

**输出:**
![](img/4c5bc39ce039955a13494c3e63ecd83f.png)
正如我们在输出中看到的，`Series.get()`函数已经返回了与传递的索引标签对应的值。

**示例 2 :** 使用`Series.get()`函数获取给定序列对象中传递的索引标签的值。

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

现在我们将使用`Series.get()`函数返回给定序列对象中传递的索引标签的值。

```py
# return the value corresponding to
# the passe index label
result = sr.get(key = '2011-03-31')

# Print the result
print(result)
```

**输出:**
![](img/cec69cc6c78d047a4dac5f189fc0799e.png)
正如我们在输出中看到的，`Series.get()`函数已经返回了与传递的索引标签对应的值。