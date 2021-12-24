# numpy.i0()函数| Python

> 原文:[https://www.geeksforgeeks.org/numpy-i0-function-python/](https://www.geeksforgeeks.org/numpy-i0-function-python/)

**`numpy.i0()`** 函数是第一类修正的贝塞尔函数，阶次为 0。通常用 I <sub>0</sub> 表示。

> **语法:** numpy.i0(x)
> **参数:**
> **x:**【array _ like，dtype float or complex】贝塞尔函数的参数。
> 
> **返回:**【n 数组，shape = x.shape，dtype = x.dtype】在 x 的每个元素上计算的修正贝塞尔函数

**代码#1 :**

```
# Python program explaining
# numpy.i0() function

# importing numpy as geek 
import numpy as geek

gfg = geek.i0(0.)

print (gfg)
```

**输出:**

```
1.0

```

**代码#2 :**

```
# Python program explaining
# numpy.i0() function

# importing numpy as geek 
import numpy as geek

gfg = geek.i0([1., 2\. + 3j])

print (gfg)
```

**输出:**

```
[ 1.26606588+0.j,  -1.24923489+0.9479838j]

```