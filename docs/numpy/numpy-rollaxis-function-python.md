# numpy.rollaxis()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-roll axis-function-python/](https://www.geeksforgeeks.org/numpy-rollaxis-function-python/)

**`numpy.rollaxis()`** 功能向后滚动指定的轴，直到它位于给定的位置。

> **语法:** numpy.rollaxis(arr，axis，start=0)
> **参数:**
> **arr:**【ndarray】输入数组。
> **轴:**【int】轴向后滚动。其他轴的位置相对于彼此不变。
> **开始:**【int，可选】轴滚动到位于该位置之前。默认值 0 导致“完全”滚动。
> **Return:**【ndarray】在早期的 NumPy 版本中，只有当轴的顺序改变时才返回 arr，否则返回输入数组。对于 NumPy > = 1.10.0，总是返回 arr 的视图。

**代码#1 :**

```
# Python program explaining
# numpy.rollaxis() function

# importing numpy as geek 
import numpy as geek

arr = geek.ones((1, 2, 3, 4))

gfg = geek.rollaxis(arr, 3, 1).shape

print (gfg)
```

**输出:**

```
(1, 4, 2, 3)

```

**代码#2 :**

```
# Python program explaining
# numpy.rollaxis() function

# importing numpy as geek 
import numpy as geek

arr = geek.ones((1, 2, 3, 4))

gfg = geek.rollaxis(arr, 2).shape

print (gfg)
```

**输出:**

```
(3, 1, 2, 4)

```