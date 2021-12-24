# Numpy recarray.partition()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-partition-function-python/](https://www.geeksforgeeks.org/numpy-recarray-partition-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.partition()`** 函数重新排列数组中的元素，使第 k 个位置的元素值处于排序数组中的位置。所有小于第 k 个元素的元素都移动到这个元素之前，所有相等或更大的元素都移动到它的后面。

> **语法:** `numpy.recarray.argpartition(kth, axis=-1, kind='introselect', order=None)`
> 
> **参数:**
> **kth:**【int 或 ints 序列】要分区的元素索引。第 k 个元素值将处于其最终的排序位置，所有较小的元素将在其之前移动，所有相等或更大的元素将在其之后移动。
> **轴:**【int 或 None】要排序的轴。如果为“无”，则数组在排序前被展平。默认值为-1，沿最后一个轴排序。
> **种类:**选择算法。默认值为“introselect”。
> **顺序:**【字符串或字符串列表】当 arr 是定义了字段的数组时，此参数指定首先比较哪些字段，其次比较哪些字段等。
> 
> **返回:**【n 数组】与 arr 类型和形状相同的分区数组。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.partition() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([(5.0, 2), (3.0, -4), (6.0, 9),
                     (9.0, 1), (5.0, 4), (-12.0, -7)],
                     dtype =[('a', float), ('b', int)])

print ("Input array : ", in_arr)

# convert it to a record array,
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of float: ", rec_arr.a)
print("Record array of int: ", rec_arr.b)

# applying recarray.partition methods
# to float record array 
rec_arr.a.partition(kth = 3)
print ("Output partitioned float array : ", rec_arr.a) 

# applying recarray.partition methods 
# to int record array 
rec_arr.b.partition(kth = 4)
print ("Output partitioned int array : ", rec_arr.b) 
```

**Output:**

```
Input array :  [(  5.,  2) (  3., -4) (  6.,  9) (  9.,  1) (  5.,  4) (-12., -7)]
Record array of float:  [  5\.   3\.   6\.   9\.   5\. -12.]
Record array of int:  [ 2 -4  9  1  4 -7]
Output partitioned float array :  [  5\. -12\.   3\.   5\.   9\.   6.]
Output partitioned int array :  [ 1 -7 -4  2  4  9]

```

**代码#2 :**

我们将`numpy.recarray.partition()`应用于整个记录数组。

```
# Python program explaining
# numpy.recarray.partition() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, 4), (6.0, -7)],
                    [(9.0, 1), (6.0, 4), (-2.0, -7)]],
                    dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr)

# convert it to a record array, 
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)

# applying recarray.partition methods to record array
rec_arr.partition(kth = 2)

print ("Output array : ", rec_arr)
```

**Output:**

```
Input array :  [[(5.0, 2) (3.0, 4) (6.0, -7)]
 [(9.0, 1) (6.0, 4) (-2.0, -7)]]
Output array :  [[(3.0, 4) (5.0, 2) (6.0, -7)]
 [(-2.0, -7) (6.0, 4) (9.0, 1)]]

```