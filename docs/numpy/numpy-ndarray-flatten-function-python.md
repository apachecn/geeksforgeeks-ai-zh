# Numpy ndarray . flat()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-ndarray-flat-function-python/](https://www.geeksforgeeks.org/numpy-ndarray-flatten-function-python/)

**`numpy.ndarray.flatten()`** 函数返回一个折叠成一维的副本数组。

> **语法:** numpy.ndarray .扁平化(顺序='C ')
> 
> **参数:**
> **顺序:** [{'C '，' F '，' A '，' K'}，可选的“' C '表示按行-主(C-style)顺序展平。“f”表示按列长(Fortran 风格)顺序展平。如果在内存中是 Fortran 连续的，则“a”表示按主要列顺序展平，否则按主要行顺序展平。“k”的意思是按照元素在内存中出现的顺序将 a 展平。默认值为“C”。
> 
> **返回:**【n 数组】输入数组的副本，展平到一维。

**代码#1 :**

```py
# Python program explaining
# numpy.ndarray.flatten() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[5, 6], [7, 8]])

gfg = arr.flatten()

print( gfg )
```

**输出:**

```py
[5 6 7 8]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ndarray.flatten() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[5, 6], [7, 8]])

gfg = arr.flatten('F')

print( gfg )
```

**输出:**

```py
[5 6 7 8]

```