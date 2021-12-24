# numpy.find_common_type()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-find _ common _ type-function-python/](https://www.geeksforgeeks.org/numpy-find_common_type-function-python/)

**`numpy.find_common_type()`** 功能确定遵循标准强制规则的常见类型。

> **语法:**numpy . find _ common _ type(array _ type，scalar _ types)
> 
> **参数:**
> **数组 _ 类型:**【序列】表示数组的数据类型或数据类型可转换对象的列表。
> **标量 _ 类型:**【序列】表示标量的数据类型或数据类型可转换对象的列表。
> **返回:**【dtype】常用数据类型，即 array _ types 忽略 scalar _ type 的最大值，除非 scalar _ type 的最大值属于不同的种类。

**代码#1 :**

```py
# Python program explaining
# numpy.find_common_type() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.find_common_type([geek.float32], [geek.int64, geek.float64])

print (gfg)
```

**输出:**

```py
float32

```

**代码#2 :**

```py
# Python program explaining
# numpy.find_common_type() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.find_common_type([geek.float32], [complex])

print (gfg)
```

**输出:**

```py
complex128

```