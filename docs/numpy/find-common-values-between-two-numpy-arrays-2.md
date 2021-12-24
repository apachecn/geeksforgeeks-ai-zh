# 找出两个 NumPy 数组之间的公共值

> 原文:[https://www . geeksforgeeks . org/find-common-values-two-numpy-arrays-2/](https://www.geeksforgeeks.org/find-common-values-between-two-numpy-arrays-2/)

在本文中，我们将讨论如何找出 2 个数组之间的公共值。为了找到公共值，我们可以使用[numpy . intersec1d()](https://www.geeksforgeeks.org/numpy-intersect1d-function-in-python/)，它将执行交集操作，并按排序顺序返回两个数组之间的公共值。

> ***语法:**numpy . intersec1d(arr 1，arr2，假定 _unique = False，return _ indexs = False)*
> 
> ***参数:***
> ***arr1、arr 2:**【array _ like】输入数组。*
> ***假设 _ 唯一:**【bool】如果为 True，则输入数组都假设为唯一，这样可以加快计算速度。默认值为假。*
> ***return _ indexes:**【bool】如果为真，则返回两个数组交集对应的索引。如果有多个值，则使用值的第一个实例。默认值为假。*
> 
> ***返回:**【ndarray】排序后的 1D 阵共有元素和独特元素。*

**示例#1:** 查找 1d 数组之间的公共值

## 蟒蛇 3

```py
import numpy as np

# create 2 arrays
a = np.array([2, 4, 7, 1, 4])
b = np.array([7, 2, 9, 0, 5])

# Display the arrays
print("Original arrays", a, ' ', b)

# use the np.intersect1d method
c = np.intersect1d(a, b)

# Display result
print("Common values", c)
```