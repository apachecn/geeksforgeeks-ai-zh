# 如何连接两个或更多熊猫数据帧？

> 原文:[https://www . geeksforgeeks . org/如何连接两个或更多熊猫-数据框/](https://www.geeksforgeeks.org/how-to-concatenate-two-or-more-pandas-dataframes/)

让我们了解如何连接两个或多个数据帧。两个或多个数据帧的连接可以使用 [pandas.concat()](https://www.geeksforgeeks.org/pandas-concat-function-in-python/) 方法完成。pandas 中的 concat()通过跨行或列组合数据框来工作。我们可以沿着行(轴=0)或沿着列(轴=1)连接两个或多个数据框

**第一步:**导入 numpy 和 pandas 库。

## 蟒 3

```
import pandas as pd
import numpy as np
```