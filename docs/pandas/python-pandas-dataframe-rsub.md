# python | pandas data frame . rsub()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫 dataframe-rsub/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**dataframe.rsub()**`函数用于寻找数据帧和其他元素的减法(二进制运算符 rfloordiv)。该功能与执行其他数据框基本相同，但支持替换其中一个输入中缺失的数据。

> **语法:** DataFrame.rsub(other，axis='columns '，level=None，fill_value=None)
> **参数:**
> **other :** Series，DataFrame，或常量
> **axis :** 对于 Series 输入，axis 要匹配
> **级别上的 Series 索引:**跨级别广播，匹配传递的 MultiIndex 级别上的索引值
> **fill_value :** 填充现有如果两个相应数据框位置的数据都丢失，结果也将丢失。
> 
> **返回:**结果:数据帧

**示例#1:** 使用`rsub()`函数将序列中的每个元素减去列轴上数据框中的相应值。

```
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

```
# importing pandas as pd
import pandas as pd

# Create the series
sr = pd.Series([12, 25, 64, 18], index =["A", "B", "C", "D"])

# Print the series
sr
```

![](img/a558e26fcf69fbbe10312e5e1070fd43.png)

让我们使用`dataframe.rsub()`函数用数据框中的相应元素减去一系列中的每个元素。

```
# equivalent to sr - df
df.rsub(sr, axis = 1)
```

**输出:**
![](img/9dc4f4760bb97b5360d68fd4782d62b5.png)

**示例 2:** 使用`rsub()`函数将数据帧中的每个元素与其他数据帧中的相应元素相减

```
# importing pandas as pd
import pandas as pd

# Creating the first dataframe 
df1 = pd.DataFrame({"A":[1, 5, 3, 4, 2],
                    "B":[3, 2, 4, 3, 4],
                    "C":[2, 2, 7, 3, 4], 
                    "D":[4, 3, 6, 12, 7]},
                     index =["A1", "A2", "A3", "A4", "A5"])

# Creating the second dataframe
df2 = pd.DataFrame({"A":[10, 11, 7, 8, 5], 
                    "B":[21, 5, 32, 4, 6], 
                    "C":[11, 21, 23, 7, 9],
                    "D":[1, 5, 3, 8, 6]}, 
                     index =["A1", "A2", "A3", "A4", "A5"])

# Print the first dataframe
print(df1)

# Print the second dataframe
print(df2)
```

![](img/e3baabcb070182605e75dbca5770baab.png)
![](img/c6c622821d13240e629dfaf3701d6166.png)

让我们执行`df2 - df1`

```
# subtract df1 from df2
df1.rsub(df2)
```

**输出:**
![](img/555b9c6404e5f1c2d609158579ee7ca4.png)