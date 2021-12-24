# 如何选择熊猫数据框的单列？

> 原文:[https://www . geesforgeks . org/如何选择-熊猫单列-数据框/](https://www.geeksforgeeks.org/how-to-select-single-column-of-a-pandas-dataframe/)

在本文中，我们将讨论如何在数据框中选择一列。现在让我们尝试使用 Python 来实现这一点。

首先，让我们创建一个数据框

## python 3

```py
# importing pandas as library
import pandas as pd

# creating data frame:
df = pd.DataFrame({'name': ['Akash', 'Ayush', 'Ashish',
                            'Diksha', 'Shivani'],

                   'Age': [21, 25, 23, 22, 18],

                   'Interest': ['Coding', 'Playing', 'Drawing',
                                'Akku', 'Swimming']})

print("The original data frame")
df
```