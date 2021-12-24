# 蟒蛇|熊猫系列.索引

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-index/](https://www.geeksforgeeks.org/python-pandas-series-index/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.index**`属性用于获取或设置给定系列对象的索引标签。

> **语法:**系列.索引
> 
> **参数:**无
> 
> **返回:**指数

**示例#1:** 使用`Series.index`属性为给定的序列对象设置索引标签。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['New York', 'Chicago', 'Toronto', 'Lisbon'])

# Print the series
print(sr)
```

**输出:**

![](img/f358e78e958f926b7640296d5559a37a.png)

现在我们将使用`Series.index`属性来设置给定对象的索引标签。

```
# Creating the row axis labels
sr.index = ['City 1', 'City 2', 'City 3', 'City 4'] 
```

**输出:**

![](img/4b2772771d6fb5d72c2864e9efa9f66a.png)

正如我们在输出中看到的那样，`Series.index`属性已经成功地为给定的 Series 对象设置了索引标签。

**示例#2 :** 使用`Series.index`属性获取给定系列对象的索引标签。

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

现在我们将使用`Series.index`属性来获取给定对象的索引标签。

```
# print the index labels
print(sr.index)
```

**输出:**

![](img/11d9ca1fae7b2492651c62b47178c54c.png)

正如我们在输出中看到的那样，`Series.index`属性已经成功地为给定的 Series 对象返回了索引标签。