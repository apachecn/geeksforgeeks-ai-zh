# num py . ndaarray . ndim()方法| Python

> 原文:[https://www . geesforgeks . org/numpy-ndarray-ndim-method-python/](https://www.geeksforgeeks.org/numpy-ndarray-ndim-method-python/)

**`numpy.ndarray.ndim()`** 函数返回一个数组的维数。

> **语法:**num py . ndaarray . ndim(arr)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。如果它还不是数组，则尝试转换。
> 
> **返回:**【int】返回 arr 中的维数。

**代码#1 :**

```
# Python program explaining
# numpy.ndarray.ndim() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([1, 2, 3, 4])

gfg = arr.ndim

print (gfg)
```

**输出:**

```
1

```

**代码#2 :**

```
# Python program explaining
# numpy.ndarray.ndim() function

# importing numpy as geek 
import numpy as geek

arr = [[1, 2, 3], [4, 5, 6]]

gfg = geek.ndim(arr)

print (gfg)
```

**输出:**

```
2

```