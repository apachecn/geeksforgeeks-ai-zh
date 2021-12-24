# numpy ndaarray . tobytes()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ndarray-to bytes-function-python/](https://www.geeksforgeeks.org/numpy-ndarray-tobytes-function-python/)

**`numpy.ndarray.tobytes()`** 函数构造包含数组中原始数据字节的 Python 字节。

> **语法:**num py . ndaarray . tobytes(order =‘c’)
> 
> **参数:**
> **顺序:** [{'C '，' F '，' None}，可选]多维数组的数据顺序:C，Fortran，或与原始数组相同。
> 
> **返回:**展示 arr 原始数据副本的 Python 字节。

**代码#1 :**

```
# Python program explaining
# numpy.ndarray.tobytes() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[0, 1], [2, 3]], dtype ='<u2')

gfg = arr.tobytes()

print (gfg)
```

**输出:**

```
b'\x00\x00\x01\x00\x02\x00\x03\x00'

```

**代码#2 :**

```
# Python program explaining
# numpy.ndarray.tobytes() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[0, 1], [2, 3]], dtype ='<u2')

gfg = arr.tobytes('F')

print (gfg)
```

**输出:**

```
b'\x00\x00\x02\x00\x01\x00\x03\x00'

```