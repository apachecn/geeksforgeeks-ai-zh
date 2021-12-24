# 从多索引熊猫数据框中删除特定行

> 原文:[https://www . geesforgeks . org/drop-specific-row-from-multi index-pandas-data frame/](https://www.geeksforgeeks.org/drop-specific-rows-from-multiindex-pandas-dataframe/)

在本文中，我们将学习如何从多索引数据框中删除特定的行。

首先，让我们创建多索引数据帧。步骤如下:

```py
import numpy as np
import pandas as pd

mldx_arrays = [np.array(['lion', 'lion', 'lion', 'bison',
                         'bison', 'bison', 'hawk', 'hawk',
                         'hawk']),

               np.array(['height', 'weight', 'speed',
                         'height', 'weight', 'speed',
                         'height', 'weight', 'speed'])]

# creating a multi-index dataframe
# with random data
multiindex_df = pd.DataFrame(
  np.random.randn(9, 4), index=mldx_arrays,
  columns=['Type A', 'Type B', 'Type C', 'Type D'])

multiindex_df.index.names = ['level 0', 'level 1']
multiindex_df
```