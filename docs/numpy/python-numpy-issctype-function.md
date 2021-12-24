# Python | numpy.issctype()函数

> 原文:[https://www . geesforgeks . org/python-numpy-issctype-function/](https://www.geeksforgeeks.org/python-numpy-issctype-function/)

**`numpy.issctype()`** 函数用于确定给定对象是否代表标量数据类型。如果给定对象表示标量数据类型，则返回 true，否则返回 false。

> **语法:** numpy.issctype(rep)
> 
> **参数:**
> **rep :** 任意输入。
> 
> **返回:**【布尔】检查 rep 是否为标量数据类型的布尔结果。

**代码#1 :**

```py
# Python program explaining
# numpy.issctype() function

# importing numpy
import numpy as geek

# Checking if integers are scalar type

rep = geek.int64

# output boolean value
out_val = geek.issctype(rep)
print ("Are integers scalar: ", out_val) 
```

**Output :**

```py
Are integers scalar:  True

```

**代码#2 :**

```py
# Python program explaining
# numpy.issctype() function

# importing numpy
import numpy as geek

# Checking if list is scalar type

rep =[ 1, 4, 7]

# output boolean value
out_val = geek.issctype(rep)
print ("Is list scalar: ", out_val) 
```

**Output :**

```py
Is list scalar:  False

```