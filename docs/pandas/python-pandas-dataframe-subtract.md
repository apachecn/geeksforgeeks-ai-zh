# Python | Pandas dataframe .核减()

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-减法/](https://www.geeksforgeeks.org/python-pandas-dataframe-subtract/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 **dataframe .减法()**函数用于计算 dataframe 和其他元素的减法。该功能本质上与 data frame-other 相同，但支持替换其中一个输入中缺失的数据。

> **语法:** DataFrame .减法(other，axis='columns '，level=None，fill_value=None)
> **参数:**
> **other :** Series，DataFrame，或常量
> **axis :** 对于 Series 输入，axis 要匹配
> **级别上的 Series 索引:**跨级别广播，匹配传递的 MultiIndex 级别上的索引值
> **fill_value :** 填充现有缺失如果两个相应数据框位置的数据都丢失，结果也将丢失。
> **返回:**结果:数据框

**示例#1:** 使用减法()函数将数据帧的每个元素与一系列中的相应元素相减。

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Creating the dataframe
df = pd.DataFrame({"A":[1, 5, 3, 4, 2],
                   "B":[3, 2, 4, 3, 4],
                   "C":[2, 2, 7, 3, 4],
                   "D":[4, 3, 6, 12, 7]},
                   index =["A1", "A2", "A3", "A4", "A5"])

# Print the dataframe
df
```

![](img/e3baabcb070182605e75dbca5770baab.png)

让我们创建这个系列

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Create the series
sr = pd.Series([12, 25, 64, 18], index =["A", "B", "C", "D"])

# Print the series
sr
```

![](img/a558e26fcf69fbbe10312e5e1070fd43.png)

让我们使用 dataframe .减法()函数进行减法运算。

## 蟒蛇 3

```py
# equivalent to df - sr
df.subtract(sr, axis = 1)
```