# 熊猫-蟒蛇中一列的累计和

> 原文:[https://www . geesforgeks . org/累计-熊猫一栏之和-python/](https://www.geeksforgeeks.org/cumulative-sum-of-a-column-in-pandas-python/)

使用预定义的函数 **cumsum()** ，可以很容易地计算 Pandas 中一列的累计和。

> **语法:** cumsum(轴=无，skipna =真，*args，* * * kwargs)
> **参数:**
> **轴:** {index (0)，columns (1)}
> **skipna:** 排除 NA/null 值。如果整行/整列为 NA，则结果为 NA
> **返回:**该列的累计和

**例 1:**

## 蟒蛇 3

```
import pandas as pd
import numpy as np

# Create a dataframe
df1 = pd.DataFrame({"A":[2, 3, 8, 14], 
                   "B":[1, 2, 4, 3], 
                   "C":[5, 3, 9,2]}) 

# Computing sum over Index axis
print(df1.cumsum(axis = 0))
```

**输出:**

```
    A   B   C
0   2   1   5
1   5   3   8
2  13   7  17
3  27  10  19

```

**例 2:**

## 蟒蛇 3

```
import pandas as pd
import numpy as np

# Create a dataframe
df1 = pd.DataFrame({"A":[None, 3, 8, 14], 
                   "B":[1, None, 4, 3], 
                   "C":[5, 3, 9,None]}) 

# Computing sum over Index axis
print(df1.cumsum(axis = 0, skipna = True))
```

**输出:**

```
      A    B     C
0   NaN  1.0   5.0
1   3.0  NaN   8.0
2  11.0  5.0  17.0
3  25.0  8.0   NaN

```

**例 3:**

## 蟒蛇 3

```
import pandas as pd
import numpy as np

# Create a dataframe
df1 = pd.DataFrame({"A":[2, 3, 8, 14], 
                   "B":[1, 2, 4, 3], 
                   "C":[5, 3, 9,2]}) 

# Computing sum over Index axis
print(df1.cumsum(axis = 1))
```

**输出:**

```
    A   B   C
0   2   3   8
1   3   5   8
2   8  12  21
3  14  17  19

```