# numpy.issubclass_()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-issubclass _-function-python/](https://www.geeksforgeeks.org/numpy-issubclass_-function-python/)

**`numpy.issubclass_()`** 函数用于判断一个类是否是第二类的子类。

> **语法:** numpy.issubclass_(arg1，arg2)
> 
> **参数:**
> **arg1 :** 【类】输入类。如果 arg1 是 arg2 的子类，则返回 True。
> **arg2 :** 【类或类的元组】输入类。如果是类的元组，如果 arg1 是任何元组元素的子类，则返回 True。
> **返回:**【布尔】布尔结果。arg1 是否是 arg2 的子类。

**代码#1 :**

```
# Python program explaining
# numpy.issubclass_() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.issubclass_(geek.int32, float)

print (gfg)
```

**输出:**

```
False

```

**代码#2 :**

```
# Python program explaining
# numpy.issubclass_() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.issubclass_(geek.float64, float)

print (gfg)
```

**输出:**

```
True

```