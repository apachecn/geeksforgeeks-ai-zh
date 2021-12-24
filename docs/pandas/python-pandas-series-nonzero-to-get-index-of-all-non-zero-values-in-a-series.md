# Python | Pandas Series .非零()获取一个系列中所有非零值的索引

> 原文:[https://www . geeksforgeeks . org/python-pandas-series-非零-获取所有非零值的系列索引/](https://www.geeksforgeeks.org/python-pandas-series-nonzero-to-get-index-of-all-non-zero-values-in-a-series/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫`**Series.nonzero()**`是一个没有争论的方法。就像它的名字说的，它不是从一个序列中返回非零值，而是返回所有非零值的索引。返回的一系列索引可以传递给`[iloc](https://www.geeksforgeeks.org/python-extracting-rows-using-pandas-iloc/)` 方法并返回所有非零值。

> **语法:** Series .非零()
> T3】返回类型:索引数组

**示例:**
在本例中，使用熊猫`Series()`方法从 Python 列表创建系列。该系列还包含一些零值。之后在序列上调用`nonzero()`方法，结果存储在结果变量中。结果序列然后被传递到`[iloc()](https://www.geeksforgeeks.org/python-extracting-rows-using-pandas-iloc/)`方法，以返回该索引处的所有非零值。

```py
# importing pandas module 
import pandas as pd 

# importing numpy module 
import numpy as np 

# creating list
list =[1, 0, 12, 1, 0, 4, 22, 0, 3, 9]

# creating series
series = pd.Series(list)

# calling .nonzero() method
result = series.nonzero()

# display
print(result)

# retrieving values using iloc method
values = series.iloc[result]

# display
values
```

**输出:**

```py
(array([0, 2, 3, 5, 6, 8, 9]), )
0     1
2    12
3     1
5     4
6    22
8     3
9     9
dtype: int64

```

如输出所示，返回每个非零元素的索引位置，并使用`iloc` 方法返回该位置的值。