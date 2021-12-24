# Python | Pandas series . add _ prefix()

> 原文:[https://www . geesforgeks . org/python-pandas-series-add _ prefix/](https://www.geeksforgeeks.org/python-pandas-series-add_prefix/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

Pandas `**Series.add_prefix()**`功能用于给定系列对象的每个索引标签添加前缀。

> **语法:** Series.add_prefix(前缀)
> 
> **参数:**
> **前缀:**每个标签前要添加的字符串。
> 
> **返回:**序列或数据帧

**示例#1:** 使用`Series.add_prefix()`函数为给定序列对象中的每个索引标签添加前缀。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([34, 5, 13, 32, 4, 15])

# Create the Index
index_ = ['Coca Cola', 'Sprite', 'Coke', 'Fanta', 'Dew', 'ThumbsUp']

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**

![](img/63ecd871db8890cd5c144556e8761aa2.png)

现在我们将使用`Series.add_prefix()`函数在给定序列对象中的每个索引标签之前添加字符串标签‘IPL 2019 _’。

```py
# add 'IPL 2019_' before each index labels
result = sr.add_prefix(prefix = 'IPL 2019_')

# Print the result
print(result)
```

**输出:**
![](img/5232c886252fb648e18954f62fc9ad64.png)
正如我们在输出中看到的，`Series.add_prefix()`函数已经成功地在给定序列对象中的每个索引标签之前添加了传递的字符串标签。

**示例 2 :** 使用`Series.add_prefix()`函数为给定序列对象中的每个索引标签添加前缀。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([51, 10, 24, 18, 1, 84, 12, 10, 5, 24, 0])

# Create the Index
# apply yearly frequency
index_ = pd.date_range('2010-10-09 08:45', periods = 11, freq ='Y')

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**
![](img/6e6ef914acc12f458d9a19dd18fb9476.png)

现在我们将使用`Series.add_prefix()`函数在给定序列对象中的每个索引标签之前添加字符串标签“Date_”。

```py
# add 'Date_' before each index labels
result = sr.add_prefix(prefix = 'Date_')

# Print the result
print(result)
```

**输出:**
![](img/098934a4596cb6eb57d516f16a18cf31.png)
正如我们在输出中看到的，`Series.add_prefix()`函数已经成功地在给定序列对象中的每个索引标签之前添加了传递的字符串标签。