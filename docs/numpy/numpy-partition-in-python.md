# Python 中的 numpy.partition()

> 原文:[https://www.geeksforgeeks.org/numpy-partition-in-python/](https://www.geeksforgeeks.org/numpy-partition-in-python/)

**`numpy.partition()`** 函数用于创建输入数组的分区副本，其元素以这样一种方式重新排列，即第 k 个位置的元素值位于排序数组中的位置。所有小于第 k 个元素的元素都移动到这个元素之前，所有等于或大于这个元素的元素都移动到它的后面。两个分区中元素的顺序未定义。

> **语法:** numpy.partition(arr，kth，axis=-1，kind='introselect '，order=None)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **kth:**【int 或 int 序列】要划分的元素索引。
> **轴:**【int 或 None】要沿其排序的轴。如果为“无”，则数组在排序前被展平。默认值为-1，沿最后一个轴排序。
> **种类:**选择算法。默认值为“introselect”。
> **顺序:**【字符串或字符串列表】当 arr 是定义了字段的数组时，此参数指定首先比较哪些字段，其次比较哪些字段等。
> 
> **返回:**【n 数组】与 arr 类型和形状相同的分区数组。

**代码#1 :**

```
# Python program explaining
# partition() function

import numpy as geek

# input array
in_arr = geek.array([ 2, 0,  1, 5, 4, 9])
print ("Input array : ", in_arr) 

out_arr = geek.partition(in_arr, 3)
print ("Output partitioned array : ", out_arr)
```

**Output:**

```
Input array :  [2 0 1 5 4 9]
Output partitioned array :  [0 1 2 4 5 9]

```

**代码#2 :**

```
# Python program explaining
# partition() function

import numpy as geek

# input array
in_arr = geek.array([ 2, 0,  1, 5, 4, 9, 3])
print ("Input array : ", in_arr) 

out_arr = geek.partition(in_arr, (0, 3))
print ("Output partitioned array : ", out_arr)
```

**Output:**

```
Input array :  [2 0 1 5 4 9 3]
Output partitioned array :  [0 1 2 3 4 9 5]

```