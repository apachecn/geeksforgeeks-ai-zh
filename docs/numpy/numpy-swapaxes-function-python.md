# numpy.swapaxes()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-swapaxes-function-python/](https://www.geeksforgeeks.org/numpy-swapaxes-function-python/)

**`numpy.swapaxes()`** 功能互换两轴一阵。

> **语法:** numpy.swapaxes(arr，axis1，axis2)
> **参数:**
> **arr:**【array _ like】输入数组。
> **轴 1:**【int】第一轴。
> **轴 2:**【int】第二轴。
> **返回:**【ndarray】在早期的 NumPy 版本中，只有当轴的顺序发生变化时，才会返回 arr 的视图，否则会返回输入数组。对于 NumPy > = 1.10.0，如果 arr 是一个数组，则返回 arr 的视图；否则会创建一个新数组。

**代码#1 :**

```
# Python program explaining
# numpy.swapaxes() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[2, 4, 6]])

gfg = geek.swapaxes(arr, 0, 1)

print (gfg)
```

**输出:**

```
[[2]
 [4]
 [6]]

```

**代码#2 :**

```
# Python program explaining
# numpy.swapaxes() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[[0, 1], [2, 3]], [[4, 5], [6, 7]]])

gfg = geek.swapaxes(arr, 0, 2)

print (gfg)
```

**输出:**

```
[[[0 4]
  [2 6]]
 [[1 5]
  [3 7]]]

```