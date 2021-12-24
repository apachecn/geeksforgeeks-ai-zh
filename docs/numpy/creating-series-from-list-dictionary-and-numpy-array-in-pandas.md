# 从熊猫中的列表、字典和 numpy 数组创建系列

> 原文:[https://www . geesforgeks . org/creating-series-from-list-dictionary-and-numpy-array-in-pandas/](https://www.geeksforgeeks.org/creating-series-from-list-dictionary-and-numpy-array-in-pandas/)

熊猫 [**系列**](https://www.geeksforgeeks.org/python-pandas-series/) 是一个一维标记数组，能够保存任何类型的数据(整数、字符串、浮点、python 对象等)。).轴标签统称为索引。熊猫系列只不过是 excel 表格中的一列。在本文中，我们将看到使用不同数据类型创建系列的各种方法。

### 从列表创建系列

一些值的列表形成使用列表索引作为系列索引的值系列。

## 巨蟒

```py
# import pandas as pd
import pandas as pd

# simple list
lst = ['G','E','E','K','S','F',
       'O','R','G','E','E','K','S']

# forming series
s = pd.Series(lst)

# output
print(s)
```