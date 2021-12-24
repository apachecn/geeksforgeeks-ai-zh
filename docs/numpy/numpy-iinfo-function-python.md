# numpy.iinfo()函数–Python

> 原文:[https://www.geeksforgeeks.org/numpy-iinfo-function-python/](https://www.geeksforgeeks.org/numpy-iinfo-function-python/)

**`numpy.iinfo()`** 功能显示整数类型的机器限制。

> **语法:**num py . iifo(dttype)
> 
> **参数:**
> **数据类型:**【整数类型、数据类型或实例】要获取信息的整数数据类型的种类。
> **返回:**整数类型的机器限制。

**代码#1 :**

```py
# Python program explaining
# numpy.iinfo() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.iinfo(geek.int16)

print (gfg)
```

**输出:**

```py
Machine parameters for int16
---------------------------------------------------------------
min = -32768
max = 32767
---------------------------------------------------------------

```

**代码#2 :**

```py
# Python program explaining
# numpy.iinfo() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.iinfo(geek.int32)

print (gfg)
```

**输出:**

```py
Machine parameters for int32
---------------------------------------------------------------
min = -2147483648
max = 2147483647
---------------------------------------------------------------

```