# 在熊猫系列

中将多索引连接成单索引

> 原文:[https://www . geesforgeks . org/concatenate-multi-index-in-single-index-in-pandas-series/](https://www.geeksforgeeks.org/concatenate-multiindex-into-single-index-in-pandas-series/)

在本文中，我们将看到如何在熊猫系列中将多索引连接到单个索引。**多索引**是指有多个同名索引。

创建一个样本系列:

```
# importing pandas module
import pandas as pd
import numpy as np

# Creating series data for address details
index_values = pd.Series([('sravan', 'address1'),
                          ('sravan', 'address2'),
                          ('sudheer', 'address1'),
                          ('sudheer', 'address2')])

# assigning values with integers
data = pd.Series(np.arange(1, 5),
                 index=index_values)

# display data
print(data)
```