# 如何用 NumPy 在 Python 中随机选择数组的行？

> 原文:[https://www . geeksforgeeks . org/如何随机选择带 numpy 的 python 数组中的行/](https://www.geeksforgeeks.org/how-to-randomly-select-rows-of-an-array-in-python-with-numpy/)

在本文中，我们将看到如何在 Python 中用 NumPy 随机选择数组行的两种不同方法。让我们看看不同的方法，通过这些方法我们可以选择数组中的随机行:

**方法 1:** 我们将使用功能 [shuffle()](https://www.geeksforgeeks.org/random-shuffle-function-in-python/) 。函数的作用是:随机打乱一个数组的行，然后我们将显示 2D 数组的一个随机行。

## 蟒 3

```py
# import modules
import random
import numpy as np

# create 2D array
data = np.arange(50).reshape((5, 10))

# display original array
print("Array:")
print(data)

# row manipulation
np.random.shuffle(data)

# display random rows
print("\nRandom row:")
rows = data[:1, :]
print(rows)
```