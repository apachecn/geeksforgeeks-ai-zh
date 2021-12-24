# 蟒蛇|熊猫系列.斧头

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-axes/](https://www.geeksforgeeks.org/python-pandas-series-axes/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

Pandas `**Series.axes**`属性返回给定系列对象的行轴标签列表。

> **语法:**系列轴
> 
> **参数:**无
> 
> **返回:**行轴标签列表

**示例#1:** 使用`Series.axes`属性返回给定系列对象的行轴标签。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['New York', 'Chicago', 'Toronto', 'Lisbon'])

# Creating the row axis labels
sr.index = ['City 1', 'City 2', 'City 3', 'City 4'] 

# Print the series
print(sr)
```

**输出:**

![](img/4b2772771d6fb5d72c2864e9efa9f66a.png)

现在我们将使用`Series.axes`属性返回给定序列对象的行轴标签列表。

```
# return the element at the first position
sr.axes
```

**输出:**
![](img/5a4efdd2396bb8317234e741890b73b4.png)
正如我们在输出中看到的，`Series.axes`属性返回了一个列表，其中包含给定 Series 对象的行轴标签。

**示例 2 :** 使用`Series.axes`属性返回给定 Series 对象的行轴标签。

```
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

现在我们将使用`Series.axes`属性返回给定序列对象的行轴标签列表。

```
# return the element at the first position
sr.axes
```

**输出:**

![](img/437b76609d5ba75eb0f855b34c44cc6a.png)

正如我们在输出中看到的那样，`Series.axes`属性返回了一个列表，其中包含给定序列对象的行轴标签。