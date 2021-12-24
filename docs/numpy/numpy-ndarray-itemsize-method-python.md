# numpy.ndarray.itemsize()方法| Python

> 原文:[https://www . geesforgeks . org/numpy-ndarray-itemsize-method-python/](https://www.geeksforgeeks.org/numpy-ndarray-itemsize-method-python/)

**`numpy.ndarray.itemsize()`** 函数返回一个数组元素的长度，以字节为单位。

> **语法:**num py . ndaarray . item size(arr)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> 
> **返回:**【int】一个数组元素的长度，以字节为单位

**代码#1 :**

```py
# Python program explaining
# numpy.ndarray.itemsize() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([1, 2, 3, 4], dtype = geek.float64)

gfg = arr.itemsize

print (gfg)
```

**输出:**

```py
8

```

**代码#2 :**

```py
# Python program explaining
# numpy.ndarray.itemsize() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([1, 2, 3, 4],  dtype = geek.complex128)

gfg = arr.itemsize

print (gfg)
```

**输出:**

```py
16

```