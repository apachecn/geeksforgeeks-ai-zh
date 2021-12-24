# python 中的 numpy.argpartition()

> 原文:[https://www.geeksforgeeks.org/numpy-argpartition-in-python/](https://www.geeksforgeeks.org/numpy-argpartition-in-python/)

**`numpy.argpartition()`** 函数用于创建输入数组的间接分区副本，其元素以这样的方式重新排列，即第 k 个位置的元素的值位于排序数组中的位置。所有小于第 k 个元素的元素都移动到这个元素之前，所有等于或大于这个元素的元素都移动到它的后面。两个分区中元素的顺序未定义。它返回一个与 arr 形状相同的索引数组，即`arr[index_array]`产生 arr 的一个分区。

> **语法:** numpy.argpartition(arr，kth，axis=-1，kind='introselect '，order=None)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **kth:**【int 或 int 序列】要划分的元素索引。
> **轴:**【int 或 None】要沿其排序的轴。如果为“无”，则数组在排序前被展平。默认值为-1，沿最后一个轴排序。
> **种类:**选择算法。默认值为“introselect”。
> **顺序:**【字符串或字符串列表】当 arr 是定义了字段的数组时，此参数指定首先比较哪些字段，其次比较哪些字段等。
> 
> **返回:**【index _ Array，ndarray】沿指定轴划分数组的索引数组。

**代码#1 :**

```py
# Python program explaining
# argpartition() function

import numpy as geek

# input array
in_arr = geek.array([[ 2, 0,  1], [ 5, 4, 9] ])
print ("Input array : \n", in_arr) 

out_arr = geek.argpartition(in_arr, 1, axis = 1)
print ("Output partitioned array indices :\n ", out_arr)
```

**Output:**

```py
Input array : 
 [[2 0 1]
 [5 4 9]]
Output partitioned array indices :
  [[1 2 0]
 [1 0 2]]

```

**代码#2 :**

```py
# Python program explaining
# argpartition() function

import numpy as geek

# input array
in_arr = geek.array([ 2, 0,  1, 5, 4, 3])
print ("Input array : ", in_arr) 

out_arr = geek.argpartition(in_arr, (0, 2))
print ("Output partitioned array indices: ", out_arr)
```

**Output:**

```py
Input array :  [2 0 1 5 4 3]
Output partitioned array indices:  [1 2 0 3 4 5]

```