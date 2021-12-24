# numpy.promote_types()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-promote _ types-function-python/](https://www.geeksforgeeks.org/numpy-promote_types-function-python/)

**`numpy.promote_types()`** 函数是一个对称函数，它返回具有最小大小和最小标量类型的数据类型，类型 1 和类型 2 都可以安全地转换为该数据类型。返回的数据类型始终是本机字节顺序。

> **语法:**numpy . promote _ type(type 1，type2)
> 
> **参数:**
> **类型 1 :** 【数据类型或数据类型说明符】第一个数据类型。
> **类型 2 :** 【数据类型或数据类型说明符】第二种数据类型。
> **返回:**【数据类型】返回升级后的数据类型。

**代码#1 :**

```py
# Python program explaining
# numpy.promote_types() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.promote_types('f4', 'i8')

print (gfg)
```

**输出:**

```py
float64

```

**代码#2 :**

```py
# Python program explaining
# numpy.promote_types() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.promote_types('>i8', '<c8')

print (gfg)
```

**输出:**

```py
complex128

```