# 如何删除 NumPy 数组的多行？

> 原文:[https://www . geeksforgeeks . org/如何删除多行 numpy 数组/](https://www.geeksforgeeks.org/how-to-delete-multiple-rows-of-numpy-array/)

[NumPy](https://www.geeksforgeeks.org/numpy-in-python-set-1-introduction/) 是用于处理数组的 Python 库。在 Python 中，有满足数组目的的列表，但是它们速度很慢。因此，NumPy 为我们提供了比传统 Python 列表快得多的数组对象。它们速度更快的原因是它们将数组存储在内存中一个连续的位置，不像列表那样使进程访问和操作更加高效。

有许多方法可以删除 NumPy 数组中的多行。它们如下

*   [**【numpy . delete()】**](https://www.geeksforgeeks.org/numpy-delete-python/)–numpy . delete()是 Python 中的一个函数，它返回一个新的数组，并沿着所提到的轴删除子数组。通过将轴的值保持为零，有两种可能的方法可以使用 numphy.delete()删除多行。

使用整数数组，语法: *np.delete(x，[ 0，2，3]，轴=0)*

## 蟒蛇 3

```py
import numpy as geek

# Defining the array
x = geek.arange(35).reshape(7, 5) 

print(geek.delete(x, [0, 1, 2], axis=0))
```