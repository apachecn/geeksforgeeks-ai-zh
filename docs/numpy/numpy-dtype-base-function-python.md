# numpy.dtype.base()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-dtype-base-function-python/](https://www.geeksforgeeks.org/numpy-dtype-base-function-python/)

**`numpy.dtype.base()`** 函数返回子阵列基本元素的数据类型，而不考虑它们的尺寸或形状。

> **语法:**num py . dttype . base()
> 
> **返回:**返回基本元素的数据类型。

**代码#1 :**

```
# Python program explaining
# numpy.dtype.base() function

# importing numpy as geek 
import numpy as geek 

x = geek.dtype('i2')

gfg = x.base

print (gfg)
```

**输出:**

```
int16

```

**代码#2 :**

```
# Python program explaining
# numpy.dtype.base() function

# importing numpy as geek 
import numpy as geek 

x = geek.dtype('8f')

gfg = x.base

print (gfg)
```

**输出:**

```
float32

```