# 如何用 Python 中的 NumPy 获取排序数组的索引？

> 原文:[https://www . geeksforgeeks . org/如何使用 python 中的 numpy 获取排序数组的索引/](https://www.geeksforgeeks.org/how-to-get-the-indices-of-the-sorted-array-using-numpy-in-python/)

借助 [argsort()](https://www.geeksforgeeks.org/numpy-argsort-in-python/) 方法可以得到给定数组的排序元素的索引。该函数用于使用 kind 关键字指定的算法沿给定轴执行间接排序。它返回一个与 arr 形状相同的索引数组，用于对数组进行排序。

**语法:**

```
numpy.argsort(arr, axis=-1, kind=’quicksort’, order=None)
```

**例 1:**

## 蟒蛇 3

```
import numpy as np

# Original array
array = np.array([10, 52, 62, 16, 16, 54, 453])
print(array)

# Indices of the sorted elements of a 
# given array
indices = np.argsort(array)
print(indices)
```

**输出:**

```
[ 10  52  62  16  16  54 453]
[0 3 4 1 5 2 6]

```

**例 2:**

## 蟒蛇 3

```
import numpy as np

# Original array
array = np.array([1, 2, 3, 4, 5])
print(array)

# Indices of the sorted elements of 
# a given array
indices = np.argsort(array)
print(indices)
```

**输出:**

```
[1 2 3 4 5]
[0 1 2 3 4]

```

**例 3:**

## 蟒蛇 3

```
import numpy as np 

# input 2d array 
in_arr = np.array([[ 2, 0, 1], [ 5, 4, 3]]) 
print ("Input array :\n", in_arr)  

# output sorted array indices 
out_arr1 = np.argsort(in_arr, kind ='mergesort', axis = 0) 
print ("\nOutput sorteded array indices along axis 0:\n", out_arr1) 

out_arr2 = np.argsort(in_arr, kind ='heapsort', axis = 1) 
print ("\nOutput sorteded array indices along axis 1:\n", out_arr2) 
```

**输出:**

```
Input array :
 [[2 0 1]
 [5 4 3]]

Output sorteded array indices along axis 0:
 [[0 0 0]
 [1 1 1]]

Output sorteded array indices along axis 1:
 [[1 2 0]
 [2 1 0]]

```