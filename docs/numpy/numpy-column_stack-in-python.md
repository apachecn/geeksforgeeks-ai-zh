# Python 中的 numpy.column_stack()

> 原文:[https://www.geeksforgeeks.org/numpy-column_stack-in-python/](https://www.geeksforgeeks.org/numpy-column_stack-in-python/)

**`numpy.column_stack()`** 功能用于将一维数组作为列堆叠成二维数组。它采用一系列一维数组，并将它们堆叠成列，形成一个二维数组。二维数组按原样堆叠，就像使用`hstack`功能一样。

> **语法:** numpy.column_stack(tup)
> 
> **参数:**
> **tup :** 【数组序列】包含待堆叠数组的元组。数组必须具有相同的第一维。
> **返回:**【堆叠二维数组】输入数组的堆叠二维数组。

**代码#1 :**

```
# Python program explaining
# column_stack() function

import numpy as geek

# input array
in_arr1 = geek.array(( 1, 2, 3 ))
print ("1st Input array : \n", in_arr1) 

in_arr2 = geek.array(( 4, 5, 6 ))
print ("2nd Input array : \n", in_arr2) 

# Stacking the two arrays 
out_arr = geek.column_stack((in_arr1, in_arr2))
print ("Output stacked array:\n ", out_arr)
```

**Output:**

```
1st Input array : 
 [1 2 3]
2nd Input array : 
 [4 5 6]
Output stacked array:
  [[1 4]
 [2 5]
 [3 6]]

```

**代码#2 :**

```
# Python program explaining
# column_stack() function

import numpy as geek

# input array
in_arr1 = geek.array([[ 1, 2, 3], [ -1, -2, -3]] )
print ("1st Input array : \n", in_arr1) 

in_arr2 = geek.array([[ 4, 5, 6], [ -4, -5, -6]] )
print ("2nd Input array : \n", in_arr2) 

# Stacking the two arrays 
out_arr = geek.column_stack((in_arr1, in_arr2))
print ("Output stacked array :\n ", out_arr)
```

**Output:**

```
1st Input array : 
 [[ 1  2  3]
 [-1 -2 -3]]
2nd Input array : 
 [[ 4  5  6]
 [-4 -5 -6]]
Output stacked array :
  [[ 1  2  3  4  5  6]
 [-1 -2 -3 -4 -5 -6]]

```