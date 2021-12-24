# 熊猫用空白或空串代替 NaN？

> 原文:[https://www . geesforgeks . org/replace-nan-with-blank-or-empty-string-in-pandas/](https://www.geeksforgeeks.org/replace-nan-with-blank-or-empty-string-in-pandas/)

在本文中，我们将讨论如何在 Pandas 中用空白或空字符串替换 NaN。

## 创建具有 NaN 值的数据帧以供演示

为此，我们将使用 pandas dataframe()对象创建 dataframe。

## 蟒 3

```py
# import pandas module
import pandas as pd

# import numpy module
import numpy as np

# create dataframe with 3 columns
data = pd.DataFrame({

    "name": ['sravan', np.nan, 'harsha', 'ramya'],
    "subjects": [np.nan, 'java', np.nan, 'html/php'],
    "marks": [98, np.nan, np.nan, np.nan]
})

# display
data
```