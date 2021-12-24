# 蟒蛇|熊猫系列. is _ 独特

> 原文:[https://www . geesforgeks . org/python-pandas-series-is _ unique/](https://www.geeksforgeeks.org/python-pandas-series-is_unique/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.is_unique**`属性返回一个布尔值。如果给定序列对象中的数据是唯一的，则返回`True`，否则返回`False`。

> **语法:** Series.is_unique
> 
> **参数:**无
> 
> **返回:**布尔值

**示例#1:** 使用`Series.is_unique`属性检查给定序列对象中的基础数据是否唯一。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['New York', 'Chicago', 'Toronto', 'Lisbon', 'Chicago'])

# Creating the row axis labels
sr.index = ['City 1', 'City 2', 'City 3', 'City 4', 'City 5'] 

# Print the series
print(sr)
```

**输出:**

![](img/8dfa831945631ae9b42922e0966ee48c.png)

现在我们将使用`Series.is_unique`属性来检查给定 Series 对象中的基础数据是唯一的还是包含一些重复的值。

```py
# check if underlying data is
# is unique or not
sr.is_unique
```

**输出:**

![](img/96e6b1374f483ec30914ba4779d7d2d7.png)
正如我们在输出中看到的，`Series.is_unique`属性已经返回`False`表示底层在给定的序列对象中不是唯一的。

**示例 2 :** 使用`Series.is_unique`属性检查给定序列对象中的基础数据是否唯一。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['1/1/2018', '2/1/2018', '3/1/2018', '4/1/2018'])

# Creating the row axis labels
sr.index = ['Day 1', 'Day 2', 'Day 3', 'Day 4']

# Print the series
print(sr)
```

**输出:**

![](img/a519278b0c944bba68cf9df8e3566a3b.png)

现在我们将使用`Series.is_unique`属性来检查给定 Series 对象中的基础数据是唯一的还是包含一些重复的值。

```py
# check if underlying data is
# is unique or not
sr.is_unique
```

**输出:**
![](img/1f254e9b60b8548f0a0aaa9c05b22ae6.png)
正如我们在输出中看到的，`Series.is_unique`属性已经返回`True`表示底层在给定的序列对象中是唯一的。