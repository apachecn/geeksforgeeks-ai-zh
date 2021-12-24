# 如何使用熊猫

显示数据框中的所有行

> 原文:[https://www . geeksforgeeks . org/如何使用 pandas 显示数据框中的所有行/](https://www.geeksforgeeks.org/how-to-display-all-rows-from-dataframe-using-pandas/)

在本文中，我们将讨论如何使用 Python 中的 Pandas 显示数据框中的所有行。

当您尝试打印超过预定义的要显示的行数和列数的大数据框时，结果将被截断。为了更好的理解，请看下面的例子。

## 蟒 3

```py
# importing numpy library
import pandas as pd

# importing diabetes dataset from sklearn
from sklearn.datasets import load_diabetes

# Loading diabetes dataset
data = load_diabetes()

# storing as data frame
dataframe = pd.DataFrame(data.data, columns=data.feature_names)

# printing data frame
print(dataframe)
```