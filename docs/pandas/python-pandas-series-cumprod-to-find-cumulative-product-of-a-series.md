# Python | Pandas series.cumprod()查找一个系列的累积积

> 原文:[https://www . geeksforgeeks . org/python-pandas-series-cumprod-to-find-累积系列产品/](https://www.geeksforgeeks.org/python-pandas-series-cumprod-to-find-cumulative-product-of-a-series/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Series.cumprod()**`用于寻找一个系列的累计乘积。在累计乘积中，返回序列的长度与输入序列相同，每个元素都等于当前值和所有先前值的乘积。

> **语法:** Series.cumprod(轴=无，skipna =真)
> 
> **参数:**
> **轴:**行操作为 0 或“索引”，列操作为 1 或“列”
> **skipna:** 如果为真，跳过下一个元素后的 NaN 添加。
> 
> **返回类型:**系列

**示例#1:**

在本例中，从 Python 列表中创建了一个系列。该列表还包含一个空值，`skipna` 参数保持默认值，即真。

```
# importing pandas module 
import pandas as pd 

# importing numpy module 
import numpy as np 

# making list of values 
values = [2, 10, np.nan, 4, 3, 0, 1] 

# making series from list 
series = pd.Series(values) 

# calling method 
cumprod = series.cumprod() 

# display 
cumprod
```

**输出:**

```
0      2.0
1     20.0
2      NaN
3     80.0
4    240.0
5      0.0
6      0.0
dtype: float64
```

**解释:** Cumprod 是当前值和所有先前值的乘积，因此，第一个元素总是等于调用者系列的第一个。

```
2
20 (2 x 10)
NaN (20 x NaN = NaN, Anything multiplied with NaN returns NaN)
80 (20 x 4)
240 (80 x 3)
0 (240 x 0)
0 (0 x 1)

```

**例 2:** 保持 skipna =假

在此示例中，创建了一个系列，就像上面的示例一样。但是`skipna` 参数保持为假。因此，空值不会被忽略，每次出现时都会进行比较。

```
# importing pandas module 
import pandas as pd 

# importing numpy module 
import numpy as np 

# making list of values 
values = [9, 4, 33, np.nan, 0, 1, 76, 5] 

# making series from list 
series = pd.Series(values) 

# calling method 
cumprod = series.cumprod(skipna = False) 

# display 
cumprod 
```

**输出:**

```
0       9.0
1      36.0
2    1188.0
3       NaN
4       NaN
5       NaN
6       NaN
7       NaN
dtype: float64
```

**说明:**就像上例一样，每个位置都返回当前值和所有先前值的乘积。由于 NaN 乘以任何值也是 NaN，并且 skipna 参数保持为 False，因此 NaN 出现后的所有值也是 NaN。