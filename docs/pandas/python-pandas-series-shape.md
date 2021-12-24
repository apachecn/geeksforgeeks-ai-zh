# 蟒蛇|熊猫系列.造型

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-shape/](https://www.geeksforgeeks.org/python-pandas-series-shape/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

Pandas `**Series.shape**`属性返回给定系列对象的基础数据形状的元组。

> **语法:**系列.形状
> 
> **参数:**无
> 
> **返回:**形状

**示例#1:** 使用`Series.shape`属性查找给定序列对象的底层数据的形状。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['New York', 'Chicago', 'Toronto', 'Lisbon', 'Rio'])

# Creating the row axis labels
sr.index = ['City 1', 'City 2', 'City 3', 'City 4', 'City 5'] 

# Print the series
print(sr)
```

**输出:**

![](img/f6a6d4c6b86dd815350de4f5d5bfa931.png)

现在我们将使用`Series.shape`属性来查找给定 Series 对象的底层数据的形状。

```py
# return the shape
sr.shape
```

**输出:**

![](img/2fe6898813823693951d657d368ec6b3.png)
正如我们在输出中看到的，`Series.shape`属性返回了一个元组，表示给定序列对象的底层数据的形状。

**例 2 :** 使用`Series.shape`属性找到给定序列对象的底层数据的形状。

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

现在我们将使用`Series.shape`属性来查找给定 Series 对象的底层数据的形状。

```py
# return the shape
sr.shape
```

**输出:**
![](img/bcc2768ab6e4e19d4858dc1824a762dc.png)
正如我们在输出中看到的，`Series.shape`属性已经返回了一个元组，表示给定序列对象的底层数据的形状。