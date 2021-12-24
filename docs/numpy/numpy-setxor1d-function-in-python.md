# Python 中的 numpy.setxor1d()函数

> 原文:[https://www . geesforgeks . org/numpy-setxor1d-python 中的函数/](https://www.geeksforgeeks.org/numpy-setxor1d-function-in-python/)

**`numpy.setxor1d()`** 函数查找两个数组的异或集合，并返回仅在一个(而不是两个)输入数组中排序的唯一值。

> **语法:** numpy.setxor1d(arr1，arr2，假定 _unique = False)
> 
> **参数:**
> **arr1、arr 2:**【array _ like】输入数组。
> **假设 _ 唯一:**【bool】如果为真，则输入数组都假设为唯一，这样可以加快计算速度。默认值为假。
> 
> **返回:**【ndarray】仅在一个输入数组中的唯一值的排序 1D 数组。

**代码#1 :**

```
# Python program explaining
# numpy.setxor1d() function

# importing numpy as geek 
import numpy as geek 

arr1 = [1, 2, 3, 4]
arr2 = [2, 4, 6, 8]

gfg = geek.setxor1d(arr1, arr2)

print (gfg)
```

**输出:**

```
[1 3 6 8]

```

**代码#2 :**

```
# Python program explaining
# numpy.setxor1d() function

# importing numpy as geek 
import numpy as geek 

arr1 = [1, 2, 3, 4, 5]
arr2 = [-2, -1, 0, 1, 2]

gfg = geek.setxor1d(arr1, arr2)

print (gfg)
```

**输出:**

```
[-2 -1  0  3  4  5]

```