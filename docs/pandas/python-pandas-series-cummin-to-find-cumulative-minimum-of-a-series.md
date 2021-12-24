# Python | Pandas Series.cummin()查找一个系列的累计最小值

> 原文:[https://www . geeksforgeeks . org/python-pandas-series-cummin-to-find-累计-a 系列最小值/](https://www.geeksforgeeks.org/python-pandas-series-cummin-to-find-cumulative-minimum-of-a-series/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫`**Series.cummin()**`用于寻找一个系列的累积最小值。在累积最小值中，返回序列的长度与输入序列相同，并且每个元素都等于当前元素和前一个元素之间的较小元素。

> **语法:** Series.cummin(轴=无，skipna =真)
> 
> **参数:**
> **轴:**行操作为 0 或“索引”，列操作为 1 或“列”
> **skipna:** 如果为真，跳过下一个元素后的 NaN 添加。
> 
> **返回类型:**系列

**示例#1:**
在此示例中，从 Python 列表创建了一个系列。该列表还包含一个空值，`skipna` 参数保持默认值，即真。

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
cummin = series.cummin() 

# display 
cummin
```

**输出:**

```py
0    3.0
1    3.0
2    NaN
3    3.0
4    2.0
5    0.0
dtype: float64
```

**说明:** Cummin 是当前值与之前值的比较。第一个元素总是等于调用者系列的第一个。

```py
3
3  (3<4)
NaN (Since NaN cannot be compared to integer values)
3  (3<7)
2  (2<3)
0  (0<2)

```

**例 2:** 守`skipna=False`

在此示例中，创建了一个系列，就像上面的示例一样。但是 skipna 参数保持为 False。因此，空值不会被忽略，每次出现时都会进行比较。

```py
# importing pandas module 
import pandas as pd 

# importing numpy module 
import numpy as np 

# making list of values 
values = [12, 4, 33, np.nan, 0, 1, 76, 5] 

# making series from list 
series = pd.Series(values) 

# calling method 
cummin = series.cummin(skipna = False) 

# display 
cummin 
```

**输出:**

```py
0    12.0
1     4.0
2     4.0
3     NaN
4     NaN
5     NaN
6     NaN
7     NaN
dtype: float64
```

**说明:**就像上面的例子一样，当前值和以前值的最小值存储在每个位置，直到 NaN 出现。由于 NaN 与任何东西进行比较都会返回 NaN，并且 skipna 参数保持为 False，因此它出现后的累积最小值是 NaN，因为所有值都与 NaN 进行了比较。