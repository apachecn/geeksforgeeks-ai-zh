# 蟒蛇|熊猫系列. combine_first()

> 原文:[https://www . geesforgeks . org/python-pandas-series-combine _ first/](https://www.geeksforgeeks.org/python-pandas-series-combine_first/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 **`combine_first()`** 的方法是将两个系列组合成一个。结果是两个序列的并集，如果调用者序列中有空值，则取传递序列中的值。如果两个空值都在同一个索引处，则在该索引处返回空值。

**注:**该方法不同于 [Series.combine()](https://www.geeksforgeeks.org/python-pandas-series-combine/) 以函数为参数决定输出值。

> **语法:** Series.combine_first(其他)
> 
> **参数:**
> **其他:**其他系列要结合来电者系列。
> 
> **回归类型:**熊猫系列

**示例:**
在本例中，使用熊猫`Series()`方法从列表中创建了两个系列。一些空值也通过 Numpy `np.nan`传递给每个列表。然后使用`.combine_first()`方法组合这两个系列。首先由*系列 1* 调用方法，结果存储在*结果 1* 中，然后类似地由*系列 2* 调用方法，结果存储在*结果 2* 中。然后打印两个返回的序列来比较输出。

```py
# importing pandas module  
import pandas as pd  

# importing numpy module 
import numpy as np 

# creating series 1 
series1 = pd.Series([70, 5, 0, 225, 1, 16, np.nan, 10, np.nan]) 

# creating series 2 
series2 = pd.Series([27, np.nan, 2, 23, 1, 95, 53, 10, 5]) 

# combining and returning results to variable
# calling on series1
result1 = series1.combine_first(series2)

# calling on series2
result2 = series2.combine_first(series1)

# printing result
print('Result 1:\n', result1, '\n\nResult 2:\n', result2)
```

**输出:**
如输出所示，即使同一系列被组合，但输出是不同的。这是因为`combine_first()`方法优先考虑之前的第一个系列(调用者系列)。如果该位置有空值，它将从第二个序列中获取相同索引处的值。

```py
Result 1:
 0     70.0
1      5.0
2      0.0
3    225.0
4      1.0
5     16.0
6     53.0
7     10.0
8      5.0
dtype: float64 

Result 2:
 0    27.0
1     5.0
2     2.0
3    23.0
4     1.0
5    95.0
6    53.0
7    10.0
8     5.0
dtype: float64

```