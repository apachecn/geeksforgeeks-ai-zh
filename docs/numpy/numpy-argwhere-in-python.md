# Python 中的 numpy.argwhere()

> 原文:[https://www.geeksforgeeks.org/numpy-argwhere-in-python/](https://www.geeksforgeeks.org/numpy-argwhere-in-python/)

**`numpy.argwhere()`** 函数用于查找非零数组元素的索引，按元素分组。

> **语法:** numpy.argwhere(arr)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> 
> **返回:**【n 数组】非零元素的索引。索引按元素分组。

**代码#1 :**

```
# Python program explaining
# argwhere() function

import numpy as geek

# input array
in_arr = [[ 2, 0, 7], [ 0, 5, 9]]
print ("Input array : ", in_arr) 

out_arr = geek.argwhere(in_arr)
print ("Output indices of non zero array element: \n", out_arr)
```

**Output:**

```
Input array :  [[2, 0, 7], [0, 5, 9]]
Output indices of non zero array element: 
 [[0 0]
 [0 2]
 [1 1]
 [1 2]]

```

**代码#2 :**

```
# Python program explaining
# argwhere() function

import numpy as geek

# input array
in_arr = geek.arange(8).reshape(4, 2)
print ("Input array : ", in_arr) 

out_arr = geek.argwhere(in_arr>4)
print ("Output indices greater than 4: \n", out_arr)
```

**Output:**

```
Input array :  [[0 1]
 [2 3]
 [4 5]
 [6 7]]
Output indices greater than 4: 
 [[2 1]
 [3 0]
 [3 1]]

```