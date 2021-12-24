# 熊猫–在分类数据中填充 NAn

> 原文:[https://www . geesforgeks . org/pandas-filling-nan-in-classic-data/](https://www.geeksforgeeks.org/pandas-filling-nan-in-categorical-data/)

真实世界的数据充满了缺失的值。为了解决这些问题，我们需要估算这些缺失的值，并从中得出有意义的结论。在本文中，我们将讨论如何在分类数据中填充 NaN 值。在分类特征的情况下，我们不能使用统计插补方法。

让我们首先创建一个样本数据集来理解填充缺失值的方法:

## python 3

```py
# import modules
import numpy as np
import pandas as pd

# create dataset
data = {'Id': [1, 2, 3, 4, 5, 6, 7, 8],

        'Gender': ['M', 'M', 'F', np.nan,
                   np.nan, 'F', 'M', 'F'],

        'Color': [np.nan, "Red", "Blue",
                  "Red", np.nan, "Red",
                  "Green", np.nan]}

# convert to data frame
df = pd.DataFrame(data)
display(df)
```