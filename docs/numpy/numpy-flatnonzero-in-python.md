# python 中的 numpy.flatnonzero()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-flatnonzero-in-python/

**`numpy.flatnonzero()`** 函数用于计算平坦版本 arr 中的非零指数。

> **语法:** numpy.flatnonzero(arr)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> 
> **返回:**数组
> 输出数组，包含非零的 arr.ravel()元素的索引。

**代码#1 :** 工作

```py
# Python program explaining
# flatnonzero() function

import numpy as geek
arr = geek.arange(-3, 4)

print ("Input  array : ", arr)

out_arr = geek.flatnonzero(arr)
print ("Indices of non zero elements : ", out_arr) 
```

**输出:**

```py
Input  array :  [-3 -2 -1  0  1  2  3]
Indices of non zero elements :  [0 1 2 4 5 6]

```

**代码#2 :** 使用非零元素的索引作为索引数组。

```py
# Python program using the indices of the non-zero 
# elements as an index array to extract these elements

out_arr = arr.ravel()[geek.flatnonzero(arr)]

print ("Output array of non-zero number: ", out_arr) 
```

**输出:**

```py
Output array of non-zero number:  [-3 -2 -1  1  2  3]

```