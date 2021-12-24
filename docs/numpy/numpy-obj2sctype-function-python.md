# numpy.obj2sctype()函数–python

> 原文:[https://www . geesforgeks . org/numpy-obj2sc type-function-python/](https://www.geeksforgeeks.org/numpy-obj2sctype-function-python/)

**`numpy.obj2sctype()`** 函数返回一个对象的标量数据类型或 Python 类型的 NumPy 等价物。

> **语法:** numpy.obj2sctype(rep，默认值=无)
> 
> **参数:**
> **代表:**【任意】返回类型的对象。
> **默认:**【任意，可选】如果给定，则返回类型无法确定的对象。如果没有给定，则这些对象不返回任何值。
> **返回:**【数据类型或 Python 类型】返回 rep 的数据类型

**代码#1 :**

```
# Python program explaining
# numpy.obj2sctype() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.obj2sctype(geek.float64)

print (gfg)
```

**输出:**

```
class 'numpy.float64'

```

**代码#2 :**

```
# Python program explaining
# numpy.obj2sctype() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.obj2sctype(geek.array([1.j]))

print (gfg)
```

**输出:**

```
class 'numpy.complex128'

```