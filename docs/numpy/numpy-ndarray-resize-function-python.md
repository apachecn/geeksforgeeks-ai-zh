# numpy.ndarray.resize()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-ndarray-resize-function-python/](https://www.geeksforgeeks.org/numpy-ndarray-resize-function-python/)

**`numpy.ndarray.resize()`** 功能改变阵列的形状和大小到位。

> **语法:**numpy . ndaarray . resize(new _ shape，refcheck = True)
> 
> **参数:**
> **new_shape :** 【整数元组，或 n 个整数】调整大小数组的 shape。
> **refcheck:**【bool，可选】如果为 False，将不检查引用计数。默认值为真。
> 
> **返回:**无

**代码#1 :**

```
# Python program explaining
# numpy.ndarray.resize() function

# importing numpy as geek 
import numpy as geek 

arr = geek.array([[0, 1], [2, 3]])

# this function change the shape and size
# of the array & return None
gfg = arr.resize((2, 1))

print (gfg)
```

**输出:**

```
None

```

**代码#2 :**

```
# Python program explaining
# numpy.ndarray.resize() function

# importing numpy as geek 
import numpy as geek 

arr = geek.array([[0, 1], [2, 3]], order = 'F')

# this function change the shape and size
# of the array & return None
gfg = arr.resize((2, 1))

print (gfg)
```

**输出:**

```
None

```