# python | pandas data frame . cumin()

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-cummin/](https://www.geeksforgeeks.org/python-pandas-dataframe-cummin/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**dataframe.cummin()**`用来**求任意轴上的累计最小值。**每个单元格都填充了迄今为止看到的最小值。

> **语法:** DataFrame.cummin(轴=无，skipna =真，*参数，* * * kwargs)
> 
> **参数:**
> **轴:**{索引(0)，列(1)}
> **skipna :** 排除 NA/null 值。如果整行/整列为“无”，结果将为“无”
> 
> **返回:**累计:系列

**例#1:** 使用`cummin()`函数沿指数轴求累计最小值。

```py
# importing pandas as pd
import pandas as pd

# Creating the dataframe
df = pd.DataFrame({"A":[5, 3, 6, 4],
                   "B":[11, 2, 4, 3],
                   "C":[4, 3, 8, 5],
                   "D":[5, 4, 2, 8]})

# Print the dataframe
df
```

**输出:**
![](img/84a809d03aa7bd73b1cff4e88ef6a21a.png)

现在找到索引轴上的累积最小值

```py
# To find the cumulative min
df.cummin(axis = 0)
```

**输出:**
![](img/705a4abb86ed91c495111147678f6268.png)

**例 2:** 使用`cummin()`函数沿列轴求累计最小值。

```py
# importing pandas as pd
import pandas as pd

# Creating the dataframe
df = pd.DataFrame({"A":[5, 3, 6, 4], 
                   "B":[11, 2, 4, 3],
                   "C":[4, 3, 8, 5],
                   "D":[5, 4, 2, 8]})

# To find the cumulative min along column axis
df.cummin(axis = 1)
```

**输出:**
![](img/e86baf25103524fc8fa728cdcd9ebb0b.png)

**示例#3:** 使用`cummin()`函数在具有`NaN`值的数据帧中沿索引轴查找累积最小值。

```py
# importing pandas as pd
import pandas as pd

# Creating the dataframe
df = pd.DataFrame({"A":[5, 3, None, 4],
                   "B":[None, 2, 4, 3],
                   "C":[4, 3, 8, 5], 
                   "D":[5, 4, 2, None]})

# To find the cumulative min
df.cummin(axis = 0, skipna = True)
```

**输出:**
![](img/a7c2cde3752930ba71ca6338bdb390c8.png)