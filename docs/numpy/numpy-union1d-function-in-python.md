# Python 中的 numpy.union1d()函数

> 原文:[https://www . geesforgeks . org/numpy-union 1d-python 中的函数/](https://www.geeksforgeeks.org/numpy-union1d-function-in-python/)

**`numpy.union1d()`** 函数查找两个数组的并集，并返回两个输入数组中唯一的、排序的值数组。

> **语法:** numpy.union1d(arr1，arr2)
> 
> **参数:**
> **arr1、arr 2:**【array _ like】输入数组。
> 
> **返回:**【ndarray】输入数组的唯一排序并集。

**代码#1 :**

```py
# Python program explaining
# numpy.union1d() function

# importing numpy as geek 
import numpy as geek 

arr1 = [-1, 0, 1]
arr2 = [-2, 0, 2]

gfg = geek.union1d(arr1, arr2)

print (gfg)
```

**输出:**

```py
[-2 -1  0  1  2]

```

**代码#2 :**

```py
# Python program explaining
# numpy.union1d() function

# importing numpy as geek 
import numpy as geek 

arr1 = [-3, -2, -1, 0, 1, 2, 3]
arr2 = [-5, -4, -3, 0, 3, 4, 5]

gfg = geek.union1d(arr1, arr2)

print (gfg)
```

**输出:**

```py
[-5 -4 -3 -2 -1  0  1  2  3  4  5]

```