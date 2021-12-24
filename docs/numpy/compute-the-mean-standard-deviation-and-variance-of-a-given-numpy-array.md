# 计算给定 NumPy 数组的平均值、标准差和方差

> 原文:[https://www . geeksforgeeks . org/计算给定 numpy 数组的平均标准偏差和方差/](https://www.geeksforgeeks.org/compute-the-mean-standard-deviation-and-variance-of-a-given-numpy-array/)

在 NumPy 中，我们可以通过两种方法计算给定数组沿第二轴的均值、标准差和方差:第一种是使用内置函数，第二种是通过均值、标准差和方差公式。

**方法一:使用**[**numpy . mean()**](https://www.geeksforgeeks.org/numpy-mean-in-python/)**、**[**numpy . STD()**](https://www.geeksforgeeks.org/numpy-std-in-python/)**、**[**numpy . var()**](https://www.geeksforgeeks.org/numpy-var-in-python/)

## Python

```
import numpy as np

# Original array
array = np.arange(10)
print(array)

r1 = np.mean(array)
print("\nMean: ", r1)

r2 = np.std(array)
print("\nstd: ", r2)

r3 = np.var(array)
print("\nvariance: ", r3)
```