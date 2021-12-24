# Python 中的 numpy .非零()

> 原文:[https://www.geeksforgeeks.org/numpy-nonzero-in-python/](https://www.geeksforgeeks.org/numpy-nonzero-in-python/)

**`numpy.nonzero()`** 函数用于计算非零元素的指数。

它返回一组数组，arr 的每个维度一个数组，包含该维度中非零元素的索引。
可以通过`arr[nonzero(arr)]` 得到数组中对应的非零值。要按元素而不是维度对索引进行分组，我们可以使用`transpose(nonzero(arr))`。

> **语法:** numpy .非零(arr)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> 
> **返回:**【数组的元组】非零元素的索引。

**代码#1:工作**

```py
# Python program explaining
# nonzero() function

import numpy as geek
arr = geek.array([[0, 8, 0], [7, 0, 0], [-5, 0, 1]])

print ("Input  array : \n", arr)

out_tpl = geek.nonzero(arr)
print ("Indices of non zero elements : ", out_tpl) 
```

**输出:**

> 输入数组:
> [[ 0 8 0]
> [7 0 0]
> [-5 0 1]]
> 非零元素的索引:(数组([0，1，2，2]，数据类型=int64)，数组([1，0，0，2]，数据类型=int64))

**代码#2 :**

```py
# Python program for getting
# The corresponding non-zero values:
out_arr = arr[geek.nonzero(arr)]

print ("Output array of non-zero number: ", out_arr) 
```

**输出:**

```py
Output array of non-zero number:  [ 8  7 -5  1]

```

**代码#3 :**

```py
# Python program for grouping the indices
# by element, rather than dimension

out_ind = geek.transpose(geek.nonzero(arr))

print ("indices of non-zero number: \n", out_ind) 
```

**输出:**

```py
indices of non-zero number: 
 [[0 1]
 [1 0]
 [2 0]
 [2 2]]

```