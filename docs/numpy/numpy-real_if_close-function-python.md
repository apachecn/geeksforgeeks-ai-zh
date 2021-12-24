# numpy.real_if_close()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-real _ if _ close-function-python/](https://www.geeksforgeeks.org/numpy-real_if_close-function-python/)

在这个 **`numpy.real_if_close()`** 函数中，如果复杂输入返回一个实数组，那么复杂部分接近于零。

> **语法:** numpy.real_if_close(arr，tol = 100)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **公差:**【浮动】“接近零”定义为公差。数组中元素复杂部分的机器公差。
> 
> **返回:**【ndarray】如果 arr 是真实的，arr 的类型用于输出。如果 arr 具有复杂元素，则返回的类型是 float。

**代码#1 :**

```py
# Python program explaining
# numpy.real_if_close() function

# importing numpy as geek 
import numpy as geek 

arr = [3.6 + 4e-14j]
tol = 1000

gfg = geek.real_if_close(arr, tol)

print (gfg)
```

**输出:**

```py
[3.6]

```

**代码#2 :**

```py
# Python program explaining
# numpy.real_if_close() function

# importing numpy as geek 
import numpy as geek 

arr = [3.6 + 2e-11j]
tol = 1000

gfg = geek.real_if_close(arr, tol)

print (gfg)
```

**输出:**

```py
[3.6+2.e-11j]

```