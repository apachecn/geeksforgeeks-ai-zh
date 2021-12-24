# 如何用 Python 打印整个熊猫数据框？

> 原文:[https://www . geeksforgeeks . org/如何打印整只熊猫-python 中的数据框/](https://www.geeksforgeeks.org/how-to-print-an-entire-pandas-dataframe-in-python/)

数据可视化是一种使用图形、图表、地图等视觉线索来传递数据洞察力的技术。这很有用，因为它有助于直观、容易地理解大量数据，从而做出更好的决策。当我们使用 a 打印大量 a 数据集时，它会截断。  在本文中，我们将看到如何在不截断的情况下打印整个熊猫 Dataframe 或 Series。

默认情况下，不打印完整的数据帧，如果长度超过默认长度，输出将被截断，如下所示:

## python 3

```py
import numpy as np
from sklearn.datasets import load_iris
import pandas as pd

# Loading irirs dataset
data = load_iris()
df = pd.DataFrame(data.data,
                  columns = data.feature_names)
display(df)
```