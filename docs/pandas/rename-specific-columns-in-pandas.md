# 重命名熊猫中的特定列

> 原文:[https://www . geesforgeks . org/rename-specific-columns-in-pandas/](https://www.geeksforgeeks.org/rename-specific-columns-in-pandas/)

给定一个熊猫[数据框](https://www.geeksforgeeks.org/python-pandas-dataframe/)，让我们看看如何使用各种方法重命名特定的列名。

首先，让我们创建一个数据框:

## python 3

```
# import pandas package
import pandas as pd

# defining a dictionary
d = {"Name": ["John", "Mary", "Helen"],
     "Marks": [95, 75, 99],
     "Roll No": [12, 21, 9]}

# creating the pandas data frame
df = pd.DataFrame(d)

df
```