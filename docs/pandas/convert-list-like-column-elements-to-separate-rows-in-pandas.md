# 将列表状的列元素转换为 Pandas 中的单独行

> 原文:[https://www . geesforgeks . org/convert-list-like-column-elements-to-separate-row-in-pandas/](https://www.geeksforgeeks.org/convert-list-like-column-elements-to-separate-rows-in-pandas/)

A [数据框](https://www.geeksforgeeks.org/python-pandas-dataframe/)是一种表格结构，其中数据按行和列排列。在处理真实数据时，经常会遇到具有类似列表元素的列。类似列表意味着元素的形式可以很容易地转换成列表。在本文中，我们将看到将类似列表的列元素转换为单独的行的各种方法。

首先，让我们创建一个用于所有方法的数据框架。

## 巨蟒

```py
# import Pandas library
import pandas as pd

# create dataframe with a column (names) having list-like elements
data = {'id': [1, 2, 3],
        'names': ["Tom,Rick,Hardy", "Ritu,Shalini,Anjana", "Ali,Amir"]}

df = pd.DataFrame(data)

print(df)
```