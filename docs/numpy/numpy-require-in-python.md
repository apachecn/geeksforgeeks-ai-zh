# Python 中的 numpy.require()

> 原文:[https://www.geeksforgeeks.org/numpy-require-in-python/](https://www.geeksforgeeks.org/numpy-require-in-python/)

**numpy.require()** 函数在返回正确标志满足传递到编译代码的要求时(可能通过 ctypes)对数组有用。

> **语法:** numpy.require(a，dtype =无，requirements =无)
> 
> **参数:**
> 
> **a :** 阵 _ 像
> 
> **数据类型:**数据类型
> 
> **要求:**字符串或字符串列表
> 
> 需求列表可以是以下任何一种。
> 
> *   ' F ':' F _ CONNECTED '–确保一个 Fortran 连续数组。
> *   C ':' C _ continental '–确保 C-continental 数组。
> *   a ':' ALigned '–确保数据类型对齐数组。
> *   w:“‘WRITE’–确保一个可写数组。
> *   o:“‘own data’–确保数组拥有自己的数据。
> *   e ':' ENSUREARRAY '–确保一个基数组，而不是子类。
> 
> **返回:**正常
> 
> **异常:**value error–raise value error

**代码#1:**

## 蟒蛇 3

```py
# Python program explaining
# numpy.require() function

# importing numpy
import numpy as np

# creating 4 x 4 array
data = np.arange(16).reshape(4, 4)

data.flags
```

**输出:**

```py
C_CONTIGUOUS : True
  F_CONTIGUOUS : False
  OWNDATA : False
  WRITABLE : True
  ALIGNED : True
  WRITEBACKIFCOPY : False
  UPDATEIFCOPY : False
```

**代码#2:**

## 蟒蛇 3

```py
import numpy as np

# Python program explaining
# numpy.require()
b = np.require(data, dtype=np.float32,
               requirements=['A', 'W', 'O', 'C'])
b.flags
```

**输出:**

```py
C_CONTIGUOUS : True
  F_CONTIGUOUS : False
  OWNDATA : True
  WRITABLE : True
  ALIGNED : True
  WRITEBACKIFCOPY : False
  UPDATEIFCOPY : False
```