# 用 Python 描述一个 NumPy 数组

> 原文:[https://www . geesforgeks . org/description-a-numpy-array-in-python/](https://www.geeksforgeeks.org/describe-a-numpy-array-in-python/)

[NumPy](https://www.geeksforgeeks.org/python-numpy/) 是一个用于数值计算的 Python 库。它提供了强大的多维数组作为 Python 对象以及各种数学函数。在本文中，我们将讨论在数组的描述性分析中使用的所有基本 NumPy 函数。让我们从初始化一个样本数组开始分析。

以下代码初始化一个 NumPy 数组:

## python 3

T5

```py
import numpy as np

# sample array
arr = np.array([4, 5, 8, 5, 6, 4,
                9, 2, 4, 3, 6])
print(arr)
```