# Python | Pandas data frame/series . dot()

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-series-dot/](https://www.geeksforgeeks.org/python-pandas-dataframe-series-dot/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 **`Dataframe.dot()`** 的工作方式与`mul()`方法类似，但返回的不是相乘的单独值，而是点积(每个索引处值的乘积之和)。

> **语法:**系列.点(其他)
> **参数:**
> **其他:**用于计算点积的其他系列
> 
> **返回类型:**具有更新值的系列

**示例#1:**
在此示例中，使用熊猫`Series()`方法从 Python 列表创建了两个系列。然后在 series1 上调用方法，series2 作为参数传递。结果随后存储在变量中并显示出来。

```py
# importing pandas module  
import pandas as pd  

# importing numpy module 
import numpy as np 

# creating series 1 
series1 = pd.Series([7, 5, 6, 4, 9]) 

# creating series 2 
series2 = pd.Series([1, 2, 3, 10, 2]) 

# storing in new variable
# calling .dot() method
ans = series1.dot(series2)

# display
print('Dot product = {}'.format(ans))
```

**输出:**

```py
Dot product = 93
```

**解释–**
调用者序列中的元素与传递序列中同一索引处的元素相乘。然后将所有相乘的值相加，得到点积。
如上例，系列有:

```py
[7, 5, 6, 4, 9]
[1, 2, 3, 10, 2]

Dot product = 7*1 + 5*2 + 6*3 + 4*10 + 9*2 = 7 + 10 + 18 + 40 + 18 = 93
```

**注:**如果任一序列中有空值，则净结果为 NaN。应分别使用`[dropna()](https://www.geeksforgeeks.org/python-pandas-dataframe-dropna/)`或`[fillna()](https://www.geeksforgeeks.org/python-pandas-dataframe-fillna-to-replace-null-values-in-dataframe/)`方法移除/替换 NaN 值。

**例 2 :**

```py
# import DataFrame
import pandas as pd

# using DataFrame.dot() method
gfg1 = pd.DataFrame([[1, 4], [9, 5]])
gfg2 = pd.DataFrame([[4, 3, 2, 1], [21, -3, -4, 1]])

print(gfg1.dot(gfg2))
```

**输出:**

> 0 1 2 3
> 0 88-9-14 5
> 1 141 12-2 14