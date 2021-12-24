# 蟒蛇|熊猫系列. loc

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-loc/](https://www.geeksforgeeks.org/python-pandas-series-loc/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.loc**`属性用于通过给定序列对象中的标签或布尔数组来访问一组行和列。

> **语法:** Series.loc
> 
> **参数:**无
> 
> **返回:**系列

**示例#1:** 使用`Series.loc`属性根据标签从给定的序列对象中选择一些值。

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

现在我们将使用`Series.loc`属性返回给定序列对象中所选标签的值。

```
# return the selected values.
sr.loc[['City 4', 'City 3', 'City 1']]
```

**输出:**

![](img/05a5fafe406ad3bfc4b13fd673d91aae.png)
正如我们在输出中看到的，`Series.loc`属性返回了标签被传递给它的城市的名称。

**示例 2 :** 使用`Series.loc`属性根据标签从给定的序列对象中选择一些值。

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

现在我们将使用`Series.loc`属性返回给定序列对象中所选标签的值。

```
# return the selected values.
sr.loc[['Day 4', 'Day 3', 'Day 1']]
```

**输出:**
![](img/68bfea86917cd125610787e2b18fbe2f.png)
正如我们在输出中看到的，`Series.loc`属性已经返回了标签被传递给它的城市的名称。