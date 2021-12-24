# Python | numpy.issubdtype()函数

> 原文:[https://www . geesforgeks . org/python-numpy-issubdtype-function/](https://www.geeksforgeeks.org/python-numpy-issubdtype-function/)

**`numpy.issubdtype()`** 函数用于确定第一个参数是否是第二个参数的类型层次结构中较低/相等的类型代码。如果第一个参数小于或等于，则返回 true，否则返回 false。

> **语法:** numpy.issubdtype(arg1，arg2)
> 
> **参数:**
> **arg1、arg 2:**【dtype _ like】dtype 或代表 typecode 的字符串。
> 
> **返回:**【布尔】布尔结果。

**代码#1 :**

```py
# Python program explaining
# numpy.issubdtype() function

# importing numpy
import numpy as geek

# selecting the argument

arg1 = geek.int64
arg2 = geek.int32

# output boolean value
out_val = geek.issubdtype(arg1, arg2)
print ("Is the first argument lower: ", out_val) 
```

**Output :**

```py
Is the first argument lower:  False

```

**代码#2 :**

```py
# Python program explaining
# numpy.issubdtype() function

# importing numpy
import numpy as geek

# selecting the argument

arg1 ='S2'
arg2 = geek.string_

# output boolean value
out_val = geek.issubdtype(arg1, arg2)
print ("Is the first argument lower: ", out_val) 
```

**Output :**

```py
Is the first argument lower:  True

```