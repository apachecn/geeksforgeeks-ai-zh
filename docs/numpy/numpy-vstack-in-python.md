# python 中的 numpy . vstack()

> 原文:[https://www.geeksforgeeks.org/numpy-vstack-in-python/](https://www.geeksforgeeks.org/numpy-vstack-in-python/)

**`numpy.vstack()`** 功能用于将输入数组的序列垂直堆叠，形成单个数组。

> **语法:**num py . v ack(tup)
> 
> **参数:**
> **tup :** 【数组序列】包含待堆叠数组的元组。除了第一个轴以外，数组必须沿所有轴具有相同的形状。
> 
> **返回:**【堆叠数组】输入数组的堆叠数组。

**代码#1 :**

```py
# Python program explaining
# vstack() function

import numpy as geek

# input array
in_arr1 = geek.array([ 1, 2, 3] )
print ("1st Input array : \n", in_arr1) 

in_arr2 = geek.array([ 4, 5, 6] )
print ("2nd Input array : \n", in_arr2) 

# Stacking the two arrays vertically
out_arr = geek.vstack((in_arr1, in_arr2))
print ("Output vertically stacked array:\n ", out_arr)
```

**Output:**

```py
1st Input array : 
 [1 2 3]
2nd Input array : 
 [4 5 6]
Output vertically stacked array:
  [[1 2 3]
 [4 5 6]]

```

**代码#2 :**

```py
# Python program explaining
# vstack() function

import numpy as geek

# input array
in_arr1 = geek.array([[ 1, 2, 3], [ -1, -2, -3]] )
print ("1st Input array : \n", in_arr1) 

in_arr2 = geek.array([[ 4, 5, 6], [ -4, -5, -6]] )
print ("2nd Input array : \n", in_arr2) 

# Stacking the two arrays vertically
out_arr = geek.vstack((in_arr1, in_arr2))
print ("Output stacked array :\n ", out_arr)
```

**Output:**

```py
1st Input array : 
 [[ 1  2  3]
 [-1 -2 -3]]
2nd Input array : 
 [[ 4  5  6]
 [-4 -5 -6]]
Output stacked array :
  [[ 1  2  3]
 [-1 -2 -3]
 [ 4  5  6]
 [-4 -5 -6]]

```