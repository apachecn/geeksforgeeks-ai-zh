# numpy.dtype.kind()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-dtype-kind-function-python/](https://www.geeksforgeeks.org/numpy-dtype-kind-function-python/)

**`numpy.dtype.kind()`** 功能通过识别数据的一般种类来确定字符代码。

> **语法:** numpy.dtype.kind(类型)
> 
> **参数:**
> **类型:**【数据类型】输入数据类型。
> **返回:**通过识别一般类型的数据返回字符代码。

**代码#1 :**

```py
# Python program explaining
# numpy.dtype.kind() function

# importing numpy as geek 
import numpy as geek 

dtype = geek.dtype('f4')

gfg = dtype.kind

print (gfg)
```

**输出:**

```py
f

```

**代码#2 :**

```py
# Python program explaining
# numpy.dtype.kind() function

# importing numpy as geek 
import numpy as geek 

dtype = geek.dtype('i4')

gfg = dtype.kind

print (gfg)
```

**输出:**

```py
i

```