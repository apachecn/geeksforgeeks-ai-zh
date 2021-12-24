# 在熊猫数据框中创建 NaN 值的方法

> 原文:[https://www . geeksforgeeks . org/创造方式-nan-熊猫价值观-dataframe/](https://www.geeksforgeeks.org/ways-to-create-nan-values-in-pandas-dataframe/)

让我们讨论在熊猫数据框中创建 NaN 值的方法。有多种方法可以在熊猫数据框中创建 NaN 值。它们是:

*   Use NumPy
*   Import csv file with blank value
*   Applied to _ numeric function

**方法 1:使用 NumPy**

## python 3

```
import pandas as pd
import numpy as np

num = {'number': [1,2,np.nan,6,7,np.nan,np.nan]}
df = pd.DataFrame(num)

df
```