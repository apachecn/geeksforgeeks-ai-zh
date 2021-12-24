# numpy.shares_memory()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-shares _ memory-function-python/](https://www.geeksforgeeks.org/numpy-shares_memory-function-python/)

**`numpy.shares_memory()`** 函数判断两个数组是否共享内存。

> **语法:** numpy.shares_memory(arr1，arr2，max_work = None)
> **参数:**
> **arr1，arr 2:**【ndarray】输入数组。
> **max _ work:**【int，可选】花在解决重叠问题上的精力。
> **返回:**【bool】检查两个数组是否共享内存。

**代码#1 :**

```
# Python program explaining
# numpy.shares_memory() function

# importing numpy as geek 
import numpy as geek 

arr1 = geek.array([1, 2, 3, 4])
arr2 = geek.array([5, 6, 7])

gfg = geek.shares_memory(arr1, arr2)

print (gfg)
```

**输出:**

```
False

```

**代码#2 :**

```
# Python program explaining
# numpy.shares_memory() function

# importing numpy as geek 
import numpy as geek 

arr1 = geek.array([1, 2, 3, 4])
arr2 = arr1[::2]

gfg = geek.shares_memory(arr1, arr2)

print (gfg)
```

**输出:**

```
True

```