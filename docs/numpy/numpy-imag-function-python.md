# numpy.imag()函数–Python

> 原文:[https://www.geeksforgeeks.org/numpy-imag-function-python/](https://www.geeksforgeeks.org/numpy-imag-function-python/)

**`numpy.imag()`** 函数返回复变元的虚部。

> **语法:** numpy.imag(arr)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> 
> **Return:**【n 数组或标量】复变元的虚部。如果 val 是真实的，则 val 的类型用于输出。如果 val 有复杂的元素，则返回的类型是 float。

**代码#1 :**

```py
# Python program explaining
# numpy.imag() function

# importing numpy as geek 
import numpy as geek 

arr = geek.array([1 + 3j, 5 + 7j, 9 + 11j])

gfg = arr.imag

print (gfg)
```

**输出:**

```py
[ 3\.  7\. 11.]

```

**代码#2 :**

```py
# Python program explaining
# numpy.imag() function

# importing numpy as geek 
import numpy as geek 

arr = geek.array([2 + 3j, 5 + 6j, 8 + 9j])

gfg = arr.imag

print (gfg)
```

**输出:**

```py
[3\. 6\. 9.]

```