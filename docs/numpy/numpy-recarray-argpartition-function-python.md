# Numpy recarray.argpartition()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-arg partition-function-python/](https://www.geeksforgeeks.org/numpy-recarray-argpartition-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.argpartition()`** 函数返回分割该数组的索引。

> **语法:** `numpy.recarray.argpartition(kth, axis=-1, kind='introselect', order=None)`
> 
> **参数:**
> **kth:**【int 或 ints 序列】要分区的元素索引。
> **轴:**【int 或 None】要排序的轴。如果为“无”，则数组在排序前被展平。默认值为-1，沿最后一个轴排序。
> **种类:**选择算法。默认值为“introselect”。
> **顺序:**【字符串或字符串列表】当 arr 是定义了字段的数组时，此参数指定首先比较哪些字段，其次比较哪些字段等。
> 
> **返回:**【index _ Array，ndarray】沿指定轴划分数组的索引数组。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.argpartition() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, -4), (6.0, 9)],
                     [(9.0, 1), (5.0, 4), (-12.0, -7)]],
                     dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr)

# convert it to a record array,
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of float: ", rec_arr.a)
print("Record array of int: ", rec_arr.b)

# applying recarray.argpartition methods
# to float record array along axis 1
out_arr = geek.recarray.argpartition(rec_arr.a, kth = 1, axis = 1)
print ("Output partitioned array indices along axis 1: ", out_arr) 

# applying recarray.argpartition methods 
# to int record array along axis 0
out_arr = geek.recarray.argpartition(rec_arr.b, kth = 1, axis = 0)
print ("Output partitioned array indices array along axis 0: ", out_arr) 
```

**Output:**

```
Input array :  [[(5.0, 2) (3.0, -4) (6.0, 9)]
 [(9.0, 1) (5.0, 4) (-12.0, -7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output partitioned array indices along axis 1:  [[1 0 2]
 [2 1 0]]
Output partitioned array indices array along axis 0:  [[1 0 1]
 [0 1 0]]

```

**代码#2 :**

我们将`numpy.recarray.argpartition()`应用于整个记录数组。

```
# Python program explaining
# numpy.recarray.argpartition() method 

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

# applying recarray.argpartition methods to  record array
out_arr = geek.recarray.argpartition(rec_arr, kth = 2)

print ("Output array : ", out_arr)
```

**Output:**

```
Input array :  [[(5.0, 2) (3.0, 4) (6.0, -7)]
 [(9.0, 1) (6.0, 4) (-2.0, -7)]]
Output array :  [[1 0 2]
 [2 1 0]]

```