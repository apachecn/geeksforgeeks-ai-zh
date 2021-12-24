# 熊猫蟒数据框的天花板和地板–向上舍入和截断

> 原文:[https://www . geesforgeks . org/ceil-and-floor-of-the-data frame-in-pandas-python-round-up-and-truncate/](https://www.geeksforgeeks.org/ceil-and-floor-of-the-dataframe-in-pandas-python-round-up-and-truncate/)

在本文中，我们将讨论获取[熊猫数据框](https://www.geeksforgeeks.org/python-pandas-dataframe/)的天花板和地板值。首先，让我们创建一个数据框架。

**例:**

## 蟒 3

```py
# importing pandas and numpy
import pandas as pd
import numpy as np

# Creating a DataFrame
df = pd.DataFrame({'Student Name': ['Anuj', 'Ajay', 'Vivek',
                                    'suraj', 'tanishq', 'vishal'],
                   'Marks': [55.3, 82.76, 95.23, 98.12,
                             95.78, 90.56]})

df
```