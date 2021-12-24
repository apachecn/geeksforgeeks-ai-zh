# 蟒蛇|熊猫系列. pow()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-pow/](https://www.geeksforgeeks.org/python-pandas-series-pow/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 **`Series.pow()`** 是一系列数学运算方法。这用于将传递序列的每个元素作为调用者序列的指数幂，并返回结果。为此，两个序列的索引必须相同，否则将返回错误。

> **语法:** Series.pow(other，=None，fill_value=None，axis=0)
> 
> **参数:**
> **其他:**其他系列或列表类型作为指数幂放入调用者系列
> **级别:**操作前系列/列表中要用 NaN 替换的值
> **填充 _ 值:**多指标情况下级别的整数值
> 
> **返回:**以其他系列为指数幂的调用者系列的值

**示例#1:**
在本例中，使用熊猫创建了两个系列。Series()方法。没有一个系列具有空值。第二个系列直接作为其他参数传递，以在操作后返回值。

```py
# importing pandas module
import pandas as pd

# creating first series
first =[1, 2, 5, 6, 3, 4]

# creating second series
second =[5, 3, 2, 1, 3, 2]

# making series
first = pd.Series(first)

# making series
second = pd.Series(second)

# calling .pow()
result = first.pow(second)

# display
result
```

**输出:**
如输出所示，返回值等于第一序列，第二序列为其指数幂。

```py
0     1
1     8
2    25
3     6
4    27
5    16
dtype: int64

```

**示例 2:** 处理空值

在本例中，还使用 numpy.nan 方法将 NaN 值放入序列中。之后，将 2 传递给 fill_value 参数，用 2 替换空值。

```py
# importing pandas module
import pandas as pd

# importing numpy module
import numpy as np

# creating first series
first =[1, 2, 5, 6, 3, np.nan, 4, np.nan]

# creating second series
second =[5, np.nan, 3, 2, np.nan, 1, 3, 2]

# making series
first = pd.Series(first)

# making seriesa
second = pd.Series(second)

# value for null replacement
null_replacement = 2

# calling .pow()
result = first.pow(second, fill_value = null_replacement)

# display
result
```

**输出:**
如输出所示，在操作之前，所有 NaN 值都被替换为 2，返回的结果中没有任何 Null 值。

```py
0      1.0
1      4.0
2    125.0
3     36.0
4      9.0
5      2.0
6     64.0
7      4.0
dtype: float64
```