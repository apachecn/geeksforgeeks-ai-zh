# 蟒蛇|熊猫系列. nbytes

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-nbytes/](https://www.geeksforgeeks.org/python-pandas-series-nbytes/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

Pandas `**Series.nbytes**`属性是返回给定 Series 对象中存储底层数据所需的字节数。

> **语法:** Series.nbytes
> 
> **参数:**无
> 
> **返回:**字节数

**示例#1:** Use `Series.nbytes`属性用于查找存储给定 Series 对象的底层数据所需的字节数。

```
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

现在我们将使用`Series.nbytes`属性来查找存储给定 Series 对象的底层数据所需的字节数。

```
# return the number of bytes
sr.nbytes
```

**输出:**

![](img/ed11f6764ba26f7da447b5ff225e0f0c.png)

我们可以在输出中看到，`Series.nbytes`属性返回了 40，表示存储给定系列对象所需的内存是 40 字节。

**示例 2 :** 使用`Series.nbytes`属性来查找存储给定 Series 对象的底层数据所需的字节数。

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

现在我们将使用`Series.nbytes`属性来查找存储给定 Series 对象的底层数据所需的字节数。

```
# return the number of bytes
sr.nbytes
```

**输出:**
![](img/66ce7bfff597799dfcfadf8dd5fee2e3.png)
正如我们在输出中看到的，`Series.nbytes`属性返回了 32，表示存储给定系列对象所需的内存是 32 字节。