# 蟒蛇|熊猫系列. ndim

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-ndim/](https://www.geeksforgeeks.org/python-pandas-series-ndim/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

Pandas `**Series.ndim**`属性返回底层数据的维数，定义为系列对象为 1。

> **语法:** Series.ndim
> 
> **参数:**无
> 
> **返回:**维度

**示例#1:** 使用`Series.ndim`属性查找给定系列对象的维度。

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

现在我们将使用`Series.ndim`属性来查找给定 Series 对象的维度。

```py
# return the dimension
sr.ndim
```

**输出:**

![](img/5477fecb9e514c3d98f150f487149d06.png)

我们可以在输出中看到，`Series.ndim`属性已经返回 1，表示给定序列对象的维度为 1。

**例 2 :** 使用`Series.ndim`属性查找给定系列对象的维度。

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

现在我们将使用`Series.ndim`属性来查找给定 Series 对象的维度。

```py
# return the dimension
sr.ndim
```

**输出:**
![](img/5477fecb9e514c3d98f150f487149d06.png)