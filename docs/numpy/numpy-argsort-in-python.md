# python 中的 numpy.argsort()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-argsort-in-python/

**`numpy.argsort()`** 函数用于使用 kind 关键字指定的算法沿给定轴执行间接排序。它返回一个与 arr 形状相同的索引数组，用于对数组进行排序。

> **语法:** numpy.argsort(arr，axis=-1，kind='quicksort '，order=None)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **轴:**【int 或 None】要排序的轴。如果为“无”，则数组在排序前被展平。默认值为-1，沿最后一个轴排序。
> **种类:** ['快速排序'，' mergesort '，' heap sort ']选择算法。默认值为“快速排序”。
> **顺序:**【字符串或字符串列表】当 arr 是定义了字段的数组时，此参数指定首先比较哪些字段，其次比较哪些字段等。
> 
> **返回:**【index _ Array，ndarray】沿指定轴排序的索引数组。如果 arr 是一维的，那么 arr[index_array]返回一个排序后的 arr。

**代码#1 :**

```
# Python program explaining
# argpartition() function

import numpy as geek

# input array
in_arr = geek.array([ 2, 0,  1, 5, 4, 1, 9])
print ("Input unsorted array : ", in_arr) 

out_arr = geek.argsort(in_arr)
print ("Output sorted array indices : ", out_arr)
print("Output sorted array : ", in_arr[out_arr])
```

**Output:**

```
Input unsorted array :  [2 0 1 5 4 1 9]
Output sorted array indices :  [1 2 5 0 4 3 6]
Output sorted array :  [0 1 1 2 4 5 9]

```

**代码#2 :**

```
# Python program explaining
# argpartition() function

import numpy as geek

# input 2d array
in_arr = geek.array([[ 2, 0, 1], [ 5, 4, 3]])
print ("Input array : ", in_arr) 

# output sorted array indices
out_arr1 = geek.argsort(in_arr, kind ='mergesort', axis = 0)
print ("Output sorteded array indices along axis 0: ", out_arr1)
out_arr2 = geek.argsort(in_arr, kind ='heapsort', axis = 1)
print ("Output sorteded array indices along axis 1: ", out_arr2)
```

**Output:**

```
Input array :  [[2 0 1]
 [5 4 3]]
Output sorteded array indices along axis 0:  [[0 0 0]
 [1 1 1]]
Output sorteded array indices along axis 1:  [[1 2 0]
 [2 1 0]]

```