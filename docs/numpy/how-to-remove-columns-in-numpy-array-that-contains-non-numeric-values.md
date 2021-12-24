# 如何删除 Numpy 数组中包含非数值的列？

> 原文:[https://www . geesforgeks . org/如何删除包含非数值的 numpy 数组中的列/](https://www.geeksforgeeks.org/how-to-remove-columns-in-numpy-array-that-contains-non-numeric-values/)

很多时候，我们在 NumPy 数组中有非数值。这些值需要删除，这样数组就不会有这些不必要的值，看起来更体面。使用**位非运算符**和 **np.isnan()** 函数可以删除所有包含 Nan 值的列。

**例 1:**

## 蟒 3

```py
# Importing Numpy module
import numpy as np

# Creating 2X3 2-D Numpy array
n_arr = np.array([[10.5, 22.5, np.nan],
                  [41, 52.5, np.nan]])

print("Given array:")
print(n_arr)

print("\nRemove all columns containing non-numeric elements ")
print(n_arr[:, ~np.isnan(n_arr).any(axis=0)])
```