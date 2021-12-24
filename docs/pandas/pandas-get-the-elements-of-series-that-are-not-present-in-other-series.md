# 熊猫–获得其他系列中不存在的系列元素

> 原文:[https://www . geesforgeks . org/pandas-获取其他系列中不存在的系列元素/](https://www.geeksforgeeks.org/pandas-get-the-elements-of-series-that-are-not-present-in-other-series/)

有时我们有两个或更多的系列，我们必须找到所有那些在一个系列中存在但在其他系列中不存在的元素。我们可以很容易地做到这一点，使用 [**逐位非运算符**](https://www.geeksforgeeks.org/python-bitwise-operators/) 以及[**pandas . isin()**](https://www.geeksforgeeks.org/python-pandas-series-isin/)**功能。**

**例 1:** 取**两个整数**系列

T5

## 蟒 3

T8T10】

```
# Importing pandas library
import pandas as pd

# Creating 2 pandas Series
ps1 = pd.Series([2, 4, 8, 20, 10, 47, 99])
ps2 = pd.Series([1, 3, 6, 4, 10, 99, 50])

print("Series1:")
print(ps1)
print("\nSeries2:")
print(ps2)

# Using Bitwise NOT operator along
# with pandas.isin()
print("\nItems of ps1 not present in ps2:")
res = ps1[~ps1.isin(ps2)]
print(res)
```