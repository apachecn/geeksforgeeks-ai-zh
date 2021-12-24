# Python | Pandas series . search sorted()

> 原文:[https://www . geesforgeks . org/python-pandas-series-search sorted/](https://www.geeksforgeeks.org/python-pandas-series-searchsorted/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。**熊猫**就是其中的一个包，让导入和分析数据变得更加容易。

熊猫`**searchsorted()**`是排序系列的一种方法。它允许用户传递要插入到序列中的参数值，并返回可插入值的位置的*数组*，以便序列的顺序保持不变。

> **语法:** Series.searchsorted(值，边='left '，sorter=None)
> 
> **参数:**
> **值:**要插入到自身(调用者系列)
> **端的值:**“左”或“右”，分别返回值的第一个或最后一个合适位置
> **排序器:**与系列相同大小的索引数组被传递。如果排序器为“无”，调用者序列必须按升序排列，否则排序器应该是对其进行排序的索引数组。
> 
> **返回类型:**索引数组

**示例#1:**

在本例中，对排序的序列调用`searchsorted()`方法，并将 3 值作为参数传递。

```py
# importing pandas module 
import pandas as pd 

# importing numpy module 
import numpy as np 

# creating list
list =[0, 2, 3, 7, 12, 12, 15, 24]

# creating series
series = pd.Series(list)

# values to be inserted
val =[1, 7, 14]

# calling .searchsorted() method
result = series.searchsorted(value = val)

# display
result
```

**输出:**

```py
array([1, 3, 6])
```

如输出所示，返回了每个值的索引。因为 7 已经存在于序列中，所以为它返回了索引位置 6，因为默认的边参数是“left”。因此，如果值相等，它将返回左侧索引。

**例 2:** 串上的`Searchsorted()`。

在这个例子中，一些水果名称的排序序列是使用 Pandas Series 方法从 python 列表中生成的。之后，两个字符串的列表作为`searchsorted()`方法的值参数传递。

```py
# importing pandas module 
import pandas as pd 

# importing numpy module 
import numpy as np 

# creating list
data =['apple', 'banana', 'mango', 'pineapple', 'pizza']

# creating series
series = pd.Series(data)

# values to be inserted
val =['grapes', 'watermelon']

# calling .searchsorted() method
result = series.searchsorted(value = val)

# display
result
```

**输出:**

```py
array([2, 5])
```

如输出所示，为传递列表中的每个值返回索引位置，这样，如果值放在该索引处，序列的顺序将被保留。