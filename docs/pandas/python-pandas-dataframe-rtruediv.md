# python | pandas data frame . rtruediv()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫 dataframe-rtruediv/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

pandas**dataframe . rtruediv()**函数用于寻找 data frame 和其他元素的浮点除法(二进制运算符 rfloordiv)。该功能本质上与执行其他/ dataframe 相同，但支持替换其中一个输入中缺失的数据。

> **语法:** DataFrame.rtruediv(其他，轴='columns '，level=None，fill_value=None)
> **参数:**
> **其他:** Series，DataFrame，或常量
> **轴:**对于 Series 输入，轴要匹配
> **级别上的 Series 索引:**跨级别广播，匹配传递的多索引级别上的索引值
> **fill_value :** Fill 如果两个相应数据框位置的数据都丢失，结果也将丢失。
> **返回:**结果:数据框

**示例#1:** 使用 rtruediv()函数将一系列的每个元素划分为列轴上数据框中的相应值。

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

让我们使用 dataframe.rtruediv()函数将一系列元素中的每个元素与 dataframe 中的相应元素分开。

## 蟒蛇 3

```py
# equivalent to sr / df
df.rtruediv(sr, axis = 1)
```