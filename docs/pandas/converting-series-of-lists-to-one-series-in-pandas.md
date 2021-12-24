# 将熊猫系列列表转换为一个系列

> 原文:[https://www . geesforgeks . org/converting-series-of-list-to-one-series-in-pandas/](https://www.geeksforgeeks.org/converting-series-of-lists-to-one-series-in-pandas/)

让我们看看如何在熊猫中把一系列列表转换成一个系列。

首先，让我们创建一系列列表。对于这个问题，我们创建了一个包含 12 个元素的系列列表，每个列表的长度为 3，共有 4 个列表，因此元素总数为 12。当系列列表转换为一个时，它将有 12 个元素。

## 蟒 3

```
import pandas as pd
data = [[1, 2, 3], [4, 5, 6], [5, 6, 7], [9, 1, 2]]

s = pd.Series(data)
print(s)
```