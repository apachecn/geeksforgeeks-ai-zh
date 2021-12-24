# Python 中的 numpy.stack()

> 原文:[https://www.geeksforgeeks.org/numpy-stack-in-python/](https://www.geeksforgeeks.org/numpy-stack-in-python/)

**`numpy.stack()`** 函数用于沿着新的轴连接一系列相同维度的数组。axis 参数指定新轴在结果维度中的索引。例如，如果轴=0，它将是第一个维度，如果轴=-1，它将是最后一个维度。

> **语法:** numpy.stack(数组，轴)
> 
> **参数:**
> **数组:**【array _ like】相同形状的数组序列。
> **轴:**【int】输入数组沿其堆叠的结果数组中的轴。
> 
> **返回:**【堆叠数组】输入数组的堆叠数组，比输入数组多一维。

**代码#1 :**

```py
# Python program explaining
# stack() function

import numpy as geek

# input array
in_arr1 = geek.array([ 1, 2, 3] )
print ("1st Input array : \n", in_arr1) 

in_arr2 = geek.array([ 4, 5, 6] )
print ("2nd Input array : \n", in_arr2) 

# Stacking the two arrays along axis 0
out_arr1 = geek.stack((in_arr1, in_arr2), axis = 0)
print ("Output stacked array along axis 0:\n ", out_arr1)

# Stacking the two arrays along axis 1
out_arr2 = geek.stack((in_arr1, in_arr2), axis = 1)
print ("Output stacked array along axis 1:\n ", out_arr2)
```

**Output:**

```py
1st Input array : 
 [1 2 3]
2nd Input array : 
 [4 5 6]
Output stacked array along axis 0:
  [[1 2 3]
 [4 5 6]]
Output stacked array along axis 1:
  [[1 4]
 [2 5]
 [3 6]]

```

**代码#2 :**

```py
# Python program explaining
# stack() function

import numpy as geek

# input array
in_arr1 = geek.array([[ 1, 2, 3], [ -1, -2, -3]] )
print ("1st Input array : \n", in_arr1) 

in_arr2 = geek.array([[ 4, 5, 6], [ -4, -5, -6]] )
print ("2nd Input array : \n", in_arr2) 

# Stacking the two arrays along axis 0
out_arr1 = geek.stack((in_arr1, in_arr2), axis = 0)
print ("Output stacked array along axis 0:\n ", out_arr1)

# Stacking the two arrays along axis 1
out_arr2 = geek.stack((in_arr1, in_arr2), axis = 1)
print ("Output stacked array along axis 1:\n ", out_arr2)

# Stacking the two arrays along last axis 
out_arr3 = geek.stack((in_arr1, in_arr2), axis = -1)
print ("Output stacked array along last axis :\n ", out_arr3)
```

**Output:**

```py
1st Input array : 
 [[ 1  2  3]
 [-1 -2 -3]]
2nd Input array : 
 [[ 4  5  6]
 [-4 -5 -6]]
Output stacked array along axis 0:
  [[[ 1  2  3]
  [-1 -2 -3]]

 [[ 4  5  6]
  [-4 -5 -6]]]
Output stacked array along axis 1:
  [[[ 1  2  3]
  [ 4  5  6]]

 [[-1 -2 -3]
  [-4 -5 -6]]]
Output stacked array along last axis :
  [[[ 1  4]
  [ 2  5]
  [ 3  6]]

 [[-1 -4]
  [-2 -5]
  [-3 -6]]]

```