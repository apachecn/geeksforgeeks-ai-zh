# 创建一维 NumPy 数组

> 原文:[https://www . geesforgeks . org/creating-a-一维-numpy-array/](https://www.geeksforgeeks.org/creating-a-one-dimensional-numpy-array/)

**一维数组**只包含一维元素。换句话说，NumPy 数组的形状应该在元组中只包含一个值。让我们看看如何创建一维 NumPy 数组。

**方法一:**先做一个列表，然后传入**numpy . array()**

T5

## python 3

T8T10】

```
# importing the module
import numpy as np

# creating the list
list = [100, 200, 300, 400]

# creating 1-d array
n = np.array(list)
print(n)
```