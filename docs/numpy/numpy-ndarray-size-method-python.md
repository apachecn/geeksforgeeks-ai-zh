# numpy.ndarray.size()方法| Python

> 原文:[https://www . geesforgeks . org/numpy-ndarray-size-method-python/](https://www.geeksforgeeks.org/numpy-ndarray-size-method-python/)

**`numpy.ndarray.size()`** 函数返回数组中元素的个数。它等于 np.prod(a.shape)，即数组维数的乘积。

> **语法:**num py . ndaarray . size(arr)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> 
> **返回:**【int】数组中元素的个数。

**代码#1 :**

```py
# Python program explaining
# numpy.ndarray.size() function

# importing numpy as geek 
import numpy as geek

arr = geek.zeros((3, 4, 2), dtype = geek.complex128)

gfg = arr.size

print (gfg)
```

**输出:**

```py
24

```

**代码#2 :**

```py
# Python program explaining
# numpy.ndarray.size() function

# importing numpy as geek 
import numpy as geek

arr = geek.zeros((3, 4, 2), dtype = geek.complex128)

gfg = geek.prod(arr.shape)

print (gfg)
```

**输出:**

```py
24

```