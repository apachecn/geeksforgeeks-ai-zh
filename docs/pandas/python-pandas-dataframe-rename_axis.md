# Python | Pandas data frame . rename _ axis()

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-rename _ axis/](https://www.geeksforgeeks.org/python-pandas-dataframe-rename_axis/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

**`dataframe.rename_axis()`** 用于**重命名数据框**中索引或列的轴。

> **语法:** DataFrame.rename_axis(映射器，axis=0，copy=True，inplace=False)
> 
> **参数:**
> **映射器:**【标量，列表式，可选】值设置轴名属性。
> **轴:** int 或 string，默认 0
> **copy:**【iboolean，默认 True】同时复制基础数据
> **inplace :** boolean，默认 False
> 
> **返回:**已重命名:调用者类型，如果 inplace=True，则返回无

有关代码中使用的 CSV 文件的链接，请单击此处的

**示例#1:** 在 nba.csv 文件中将球队“波士顿凯尔特人”替换为“欧米茄勇士”

```py
# importing pandas as pd
import pandas as pd

# Making data frame from the csv file
df = pd.read_csv("nba.csv")

# Printing the first 10 rows of the 
# dataframe for visualization
df[:10]
```

**输出:**
![](img/836ed1d13f8962a28804f881cfca5a18.png)

我们将更改行索引，并将该值增加两倍。

```py
# this will Increase the row index value by twice
df.rename_axis(lambda x:x * 2, axis ="index")
```

**输出:**
![](img/96c8f7ff598972d7e71fe999e513fcc7.png)

**示例#2:** 更改列名

```py
# importing pandas as pd
import pandas as pd

# Making data frame from the csv file
df = pd.read_csv("nba.csv")

# this will add '_X' at the end of each column name
df.rename_axis(lambda x:x+"_X", axis ="columns")
```

**输出:**
![](img/cfad5997ce2728727cfe634564e39f69.png)