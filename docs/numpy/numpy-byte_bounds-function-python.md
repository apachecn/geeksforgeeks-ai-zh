# numpy.byte_bounds()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-byte _ bounds-function-python/](https://www.geeksforgeeks.org/numpy-byte_bounds-function-python/)

**`numpy.byte_bounds()`** 函数返回指向数组端点的指针。

> **语法:**numpy . byte _ bounds(arr)
> **参数:**
> **arr:**【ndarray】输入数组。
> **Return:**【2 个整数的元组】第一个整数是数组的第一个字节，第二个整数刚好经过数组的最后一个字节。如果 arr 不连续，它将不会使用(低、高)值之间的每个字节。

**代码#1 :**

```py
# Python program explaining
# numpy.byte_bounds() function

# importing numpy as geek 
import numpy as geek 

arr = geek.eye(2, dtype = 'f')

gfg = geek.byte_bounds(arr)

print (gfg)
```

**输出:**

```py
(37062512, 37062528)

```

**代码#2 :**

```py
# Python program explaining
# numpy.byte_bounds() function

# importing numpy as geek 
import numpy as geek 

arr = geek.eye(2)

gfg = geek.byte_bounds(arr)

print (gfg)
```

**输出:**

```py
(30421344, 30421376)

```