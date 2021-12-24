# Python 中的 numpy.sort_complex()

> 原文:[https://www.geeksforgeeks.org/numpy-sort_complex-in-python/](https://www.geeksforgeeks.org/numpy-sort_complex-in-python/)

**`numpy.sort_complex()`** 功能用于对复杂数组进行排序。它首先使用实部，然后使用虚部对数组进行排序。

> **语法:** numpy.sort_complex(arr)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> 
> **返回:**【复数组】排序后的复数组。

**代码#1 :**

```py
# Python program explaining
# sort_complex() function

import numpy as geek

# input array
in_arr = [2, 8, 7, 5, 9]
print ("Input array : ", in_arr) 

out_arr = geek.sort_complex(in_arr) 
print ("Output sorted array : ", out_arr)
```

**Output:**

```py
Input array :  [2, 8, 7, 5, 9]
Output sorted array :  [ 2.+0.j  5.+0.j  7.+0.j  8.+0.j  9.+0.j]

```

**代码#2 :**

```py
# Python program explaining
# sort_complex() function

import numpy as geek

# input array
in_arr = [2 + 4j, 5 + 9j, 3 - 2j, 4 - 3j, 3 + 5j, 2-4j, 5]
print ("Input array : ", in_arr)   

out_arr = geek.sort_complex(in_arr) 
print ("Output sorted array : ", out_arr)
```

**Output:**

```py
Input array :  [(2+4j), (5+9j), (3-2j), (4-3j), (3+5j), (2-4j), 5]
Output sorted array :  [ 2.-4.j  2.+4.j  3.-2.j  3.+5.j  4.-3.j  5.+0.j  5.+9.j]

```