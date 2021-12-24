# 如何检查 NumPy 数组中是否存在指定值？

> 原文:[https://www . geeksforgeeks . org/如何检查指定值是否存在于 numpy 数组中/](https://www.geeksforgeeks.org/how-to-check-whether-specified-values-are-present-in-numpy-array/)

有时我们需要测试数组中是否存在某些值。使用 Numpy 数组，我们可以很容易地找到特定的值是否存在。为此，我们在运算符中使用“**”。“**”运算符中的“**用于检查给定序列中是否存在某些元素和值，因此返回布尔值“**真**”和“**假**”。**

**例 1:**

## 蟒 3

```
# importing Numpy package
import numpy as np

# creating a Numpy array
n_array = np.array([[2, 3, 0],
                    [4, 1, 6]])

print("Given array:")
print(n_array)

# Checking whether specific values
# are present in "n_array" or not
print(2 in n_array)
print(0 in n_array)
print(6 in n_array)
print(50 in n_array)
print(10 in n_array)
```