# Python | Pandas Series.cumsum()求一个系列的累计和

> 原文:[https://www . geesforgeks . org/python-pandas-series-cum sum-to-find-累计-series-sum/](https://www.geeksforgeeks.org/python-pandas-series-cumsum-to-find-cumulative-sum-of-a-series/)

熊猫 **`Series.cumsum()`** 用来求一个数列的累计和。在累积和中，返回序列的长度与输入相同，并且每个元素都等于所有先前元素的总和。

> **语法:** Series.cumsum(轴=无，skipna =真)
> 
> **参数:**
> **轴:**行操作为 0 或“索引”，列操作为 1 或“列”
> **skipna:** 如果为真，跳过下一个元素后的 NaN 添加。
> 
> **结果类型:**系列

**示例#1:**
在本例中，使用 Pandas 从 Python 列表中创建了一个系列。Series()方法。该列表还包含一个空值，skipna 参数保持默认值，即 True。

```py
# importing pandas module
import pandas as pd

# importing numpy module
import numpy as np

# making list of values
values = [3, 4, np.nan, 7, 2, 0]

# making series from list
series = pd.Series(values)

# calling method
cumsum = series.cumsum()

# display
cumsum
```

**输出:**

```py
3
7
NaN
14
16
16
dtype: float64
```

**解释**
累计和是当前值和所有以前值的和。如以上输出所示，添加操作如下

```py
3
3+4 = 7
7+NaN = NaN
7+7 = 14
14+2 = 16
16+0 = 16
```

**示例#2:** skipna=False
在此示例中，创建了一个系列，就像上面的示例一样。但是`skipna` 参数保持为假。因此，空值不会被忽略，它会在每次出现后被添加。

```py
# importing pandas module
import pandas as pd

# importing numpy module
import numpy as np

# making list of values
values = [1, 20, 13, np.nan, 0, 1, 5, 23]

# making series from list
series = pd.Series(values)

# calling method
cumsum = series.cumsum(skipna = False)

# display
cumsum
```

**输出:**

```py
0     1.0
1    21.0
2    34.0
3     NaN
4     NaN
5     NaN
6     NaN
7     NaN
dtype: float64
```

**说明:**从输出中可以看出，NaN 第一次出现后的所有值也是 NaN，因为任何数字+ NaN 也是 NaN。