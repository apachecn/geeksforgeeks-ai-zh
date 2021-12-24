# numpy.maximum_sctype()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-maximum _ sc type-function-python/](https://www.geeksforgeeks.org/numpy-maximum_sctype-function-python/)

**`numpy.maximum_sctype()`** 函数返回与输入相同类型的最高精度的标量类型。

> **语法:** numpy.maximum_sctype(t)
> 
> **参数:**
> **t :** 【数据类型或数据类型说明符】输入的数据类型。这可以是一个数据类型对象，也可以是一个可转换为数据类型的对象。
> **返回:**【dtype】与输入同类的最高精度数据类型。

**代码#1 :**

```
# Python program explaining
# numpy.maximum_sctype() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.maximum_sctype(int)

print (gfg)
```

**输出:**

```
class 'numpy.int64'

```

**代码#2 :**

```
# Python program explaining
# numpy.maximum_sctype() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.maximum_sctype('f4')

print (gfg)
```

**输出:**

```
class 'numpy.float128'

```