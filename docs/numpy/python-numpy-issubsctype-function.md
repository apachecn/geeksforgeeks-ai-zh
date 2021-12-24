# python | num py . isssubsctype()函数

> 原文:[https://www . geesforgeks . org/python-numpy-issubctype-function/](https://www.geeksforgeeks.org/python-numpy-issubsctype-function/)

**`numpy.issubsctype()`** 函数用于判断第一个参数是否是第二个参数的子类。如果第一个参数是第二个参数的子类，则返回 true，否则返回 false。

> **语法:**num py . isssubsctype(arg 1，arg2)
> 
> **参数:**
> **arg1、arg2 :** 数据类型或数据类型说明符。
> 
> **返回:**【布尔】布尔结果。

**代码#1 :**

```
# Python program explaining
# numpy.issubsctype() function

# importing numpy
import numpy as geek

# selecting the argument

arg1 = geek.array([1.0, 2.5, 3.9])
arg2 = geek.int

# output boolean value
out_val = geek.issubsctype(arg1, arg2)
print ("Is the first argument subclass of the second argument: ", out_val) 
```

**Output :**

```
Is the first argument subclass of the second argument:  False

```

**代码#2 :**

```
# Python program explaining
# numpy.issubsctype() function

# importing numpy
import numpy as geek

# selecting the argument

arg1 = geek.array([1.0, 2.5, 3.9])
arg2 = geek.float

# output boolean value
out_val = geek.issubsctype(arg1, arg2)
print ("Is the first argument subclass of the second argument: ", out_val) 
```

**Output :**

```
Is the first argument subclass of the second argument:  True

```