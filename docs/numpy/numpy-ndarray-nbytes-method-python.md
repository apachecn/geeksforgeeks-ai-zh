# numpy.ndarray.nbytes()方法| Python

> 原文:[https://www . geesforgeks . org/numpy-ndarray-nbytes-method-python/](https://www.geeksforgeeks.org/numpy-ndarray-nbytes-method-python/)

**`numpy.ndarray.nbytes()`** 函数返回数组元素消耗的总字节数。

> **语法:**num py . ndaarray . nbytes(arr)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> 
> **返回:**【int】数组元素消耗的总字节数。

**代码#1 :**

```py
# Python program explaining
# numpy.ndarray.nbytes() function

# importing numpy as geek 
import numpy as geek

arr = geek.zeros((1, 2, 3), dtype = geek.complex128)

gfg = arr.nbytes

print (gfg)
```

**输出:**

```py
96

```

**代码#2 :**

```py
# Python program explaining
# numpy.ndarray.nbytes() function

# importing numpy as geek 
import numpy as geek

arr = geek.random.rand(10000, 50)

gfg = arr.nbytes

print (gfg)
```

**输出:**

```py
4000000

```