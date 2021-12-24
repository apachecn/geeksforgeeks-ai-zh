# numpy . who function–Python

> 原文:[https://www.geeksforgeeks.org/numpy-who-function-python/](https://www.geeksforgeeks.org/numpy-who-function-python/)

**`numpy.who()`** 函数打印给定字典中的 NumPy 数组。

> **语法:**numpy . who(vardict = None)
> **参数:**
> **vardict:**【dict，可选】可能包含 ndarrays 的字典。
> **返回:**返回‘无’。如果没有传入字典或 vardict 为 None，则返回 globals()字典中的 NumPy 数组。

**代码#1 :**

```
# Python program explaining
# numpy.who() function

# importing numpy as geek 
import numpy as geek 

a = geek.arange(5)
b = geek.ones(10)

gfg = geek.who()

print (gfg)
```

**输出:**

```
a               5                40               int64
b               10               80               float64

Upper bound on total bytes  =       120
None

```

**代码#2 :**

```
# Python program explaining
# numpy.who() function

# importing numpy as geek 
import numpy as geek 

a = geek.arange(3.0)
b = geek.arange(5.0)

gfg = geek.who()

print (gfg)
```

**输出:**

```
Name            Shape            Bytes            Type
===========================================================

a               3                24               float64
b               5                40               float64

Upper bound on total bytes  =       64
None

```