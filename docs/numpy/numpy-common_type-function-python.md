# numpy.common_type()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-common _ type-function-python/](https://www.geeksforgeeks.org/numpy-common_type-function-python/)

**`numpy.common_type()`** 函数返回输入数组中常见的标量类型。

> **语法:** numpy.common_type(数组)
> 
> **参数:**
> **array1、array2、…。:**【ndarrays】输入数组。
> **返回:**【dtype】返回输入数组共有的数据类型。

**代码#1 :**

```py
# Python program explaining
# numpy.common_type() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.common_type(geek.arange(2, dtype = geek.float32))

print (gfg)
```

**输出:**

```py
class 'numpy.float32'

```

**代码#2 :**

```py
# Python program explaining
# numpy.common_type() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.common_type(geek.arange(2, dtype = geek.float32), geek.arange(2))

print (gfg)
```

**输出:**

```py
class 'numpy.float64'

```