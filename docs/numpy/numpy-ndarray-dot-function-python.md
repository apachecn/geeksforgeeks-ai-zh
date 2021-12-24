# num py ndaarray . dot()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ndarray-dot-function-python/](https://www.geeksforgeeks.org/numpy-ndarray-dot-function-python/)

**`numpy.ndarray.dot()`** 函数返回两个数组的点积。

> **语法:**num py . ndaarray . dot(arr，out=None)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **输出:**【n 数组，可选】输出参数。
> 
> **返回:**【n 数组】两个数组的点积。

**代码#1 :**

```
# Python program explaining
# numpy.ndarray.dot() function

# importing numpy as geek 
import numpy as geek

arr1 = geek.eye(3)
arr = geek.ones((3, 3)) * 3

gfg = arr1.dot( arr )

print( gfg)
```

**输出:**

```
[[ 3\.  3\.  3.]
 [ 3\.  3\.  3.]
 [ 3\.  3\.  3.]]

```

**代码#2 :**

```
# Python program explaining
# numpy.ndarray.dot() function

# importing numpy as geek 
import numpy as geek

arr1 = geek.eye(3)
arr = geek.ones((3, 3)) * 3

gfg = arr1.dot(arr).dot(arr)

print( gfg)
```

**输出:**

```
[[ 27\.  27\.  27.]
 [ 27\.  27\.  27.]
 [ 27\.  27\.  27.]]

```