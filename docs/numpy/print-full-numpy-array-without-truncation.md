# 不截断打印完整 Numpy 数组

> 原文:[https://www . geeksforgeeks . org/print-full-numpy-array-不带截断/](https://www.geeksforgeeks.org/print-full-numpy-array-without-truncation/)

Numpy 是 python 的基础库，用于执行科学计算。它提供高性能多维数组和工具来处理它们。NumPy 数组是由正整数元组索引的值网格(相同类型)。Numpy 阵列速度快，易于理解，并赋予用户跨整个阵列执行计算的权利。

让我们使用简单的 NumPy 函数

## python 3

打印从 0 到 1000 的数字

```
import numpy as np
arr = np.arange(1001)
print(arr)
```