# 蟒蛇|熊猫系列. diff()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-diff/](https://www.geeksforgeeks.org/python-pandas-series-diff/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫`**Series.diff()**` 用来寻找同一系列元素之间的差异。差异是连续的，取决于传递给`diff()`方法的周期参数。

> **语法:** Series.diff(句点=1)
> 
> **参数:**
> **周期:**整数值，从当前元素中减去周期前/后元素。也接受负值
> 
> **返回类型:**系列

**示例:**
在本例中，从 Python 列表创建了两个系列。`diff()`方法在两个序列上调用，一次带正周期，一次带负值传递给周期参数。

```
# importing pandas module 
import pandas as pd 

# importing numpy module 
import numpy as np 

# creating list
list =[15, 2, 34, 12, 4, 0, 9, 7]

# creating series
series = pd.Series(list)

# calling method with period 2
period2 = series.diff(2)

# Passing Negative value to period
# passing period of -1
period_1 = series.diff(-1)

# display
print('Diff with period 2:\n{}\n\
       Diff with period -1:\n{}'.format(period2, period_1))
```

**输出:**

```
Diff with period 2:
0     NaN
1     NaN
2    19.0
3    10.0
4   -30.0
5   -12.0
6     5.0
7     7.0
dtype: float64

Diff with period -1:
0    13.0
1   -32.0
2    22.0
3     8.0
4     4.0
5    -9.0
6     2.0
7     NaN
dtype: float64
```

**说明:**在周期为 2 的第一次输出中，从第(i+2)个位置减去第 I 个位置的值，并存储在第(i+2)个位置。在第二次输出中，从第(i-1)个位置的值中减去第 I 个位置的值，并存储在第(i-1)个位置。

**注意:**输出序列中的第一个/最后一个 n 值是 NaN，取决于周期的符号。(如果周期为正，则为第一个；如果周期为负，则为最后一个，其中 n 为周期)。