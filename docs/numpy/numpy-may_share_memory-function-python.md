# numpy.may_share_memory()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-may _ share _ memory-function-python/](https://www.geeksforgeeks.org/numpy-may_share_memory-function-python/)

**`numpy.may_share_memory()`** 函数确定两个数组是否共享内存。

> **语法:** numpy.may_share_memory(arr1，arr2，max_work = None)
> **参数:**
> **arr1，arr 2:**【ndarray】输入数组。
> **max _ work:**【int，可选】花在解决重叠问题上的精力。
> **返回:**【bool】检查两个数组是否共享内存。返回真不一定意味着两个数组共享任何元素。这只是意味着他们可能。

**代码#1 :**

```py
# Python program explaining
# numpy.may_share_memory() function

# importing numpy as geek 
import numpy as geek 

arr1 = geek.array([1, 2, 3, 4])
arr2 = geek.array([5, 6, 7])

gfg = geek.may_share_memory(arr1, arr2)

print (gfg)
```

**输出:**

```py
False

```

**代码#2 :**

```py
# Python program explaining
# numpy.may_share_memory() function

# importing numpy as geek 
import numpy as geek 

arr1 = geek.zeros([3, 4])
arr2 = arr1[::1]

gfg = geek.may_share_memory(arr1, arr2)

print (gfg)
```

**输出:**

```py
True

```