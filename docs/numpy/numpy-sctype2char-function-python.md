# numpy.sctype2char()函数–python

> 原文:[https://www . geesforgeks . org/numpy-sctype2 char-function-python/](https://www.geeksforgeeks.org/numpy-sctype2char-function-python/)

**`numpy.sctype2char()`** 函数返回标量数据类型的字符串表示。

> **语法**numpy . sctypee2char(sctype)
> 
> **参数:**
> **sctype :** 【标量数据类型或对象】如果 sctype 是标量数据类型，则返回相应的字符串。如果一个对象，sctype2char 试图推断它的标量类型，然后返回相应的字符串。
> **返回:**【str】标量类型对应的字符串。

**代码#1 :**

```py
# Python program explaining
# numpy.sctype2char() function

# importing numpy as geek 
import numpy as geek 

x = geek.array([1., 2-1.j])

gfg = geek.sctype2char(x)

print (gfg)
```

**输出:**

```py
D

```

**代码#2 :**

```py
# Python program explaining
# numpy.sctype2char() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.sctype2char(list)

print (gfg)
```

**输出:**

```py
0

```