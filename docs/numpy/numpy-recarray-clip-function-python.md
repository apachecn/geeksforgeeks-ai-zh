# Numpy recarray.clip()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-clip-function-python/](https://www.geeksforgeeks.org/numpy-recarray-clip-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.clip()`** 函数返回一个值被限制在 **`[min, max]`** 的数组。必须给出最大值或最小值之一。

> **语法:** `numpy.recarray.clip(min=None, max=None, out=None)`
> 
> **参数:**
> **min :** 最小值。
> –>如果无，则不在下间隔边缘进行剪裁。最小值和最大值中最多只能有一个为无。
> **最大值:**最大值。
> –>如果无，不在上区间边缘进行裁剪。最小值和最大值中最多只能有一个为无。
> –>如果 a_min 或 a_max 是 array_like，那么这三个数组将被广播以匹配它们的形状。
> **出:**结果会放在这个数组中。它可能是就地剪辑的输入数组。out 的形状必须正确，才能容纳输出。它的类型得以保留。
> 
> **返回:**【clipped _ array，ndarray】小于最小值的值用最小值替换，大于最大值的值用最大值替换的数组。

**代码#1 :**

```py
# Python program explaining
# numpy.recarray.clip() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, -4), (6.0, 9)], [(9.0, 1), (5.0, 4), (-12.0, -7)]],
        dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr)

# convert it to a record array, using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of int: ", rec_arr.b)

# applying recarray.clip methods to float record array
float_rec_arr = rec_arr.a
print("Record array of float: ", float_rec_arr)
out_arr = (rec_arr.a).clip(min =-1.0, max = 5.0)
print ("Output clipped array : ", out_arr) 

# applying recarray.clip methods to int record array
int_rec_arr = rec_arr.b 
print("Record array of int: ", int_rec_arr)
out_arr = int_rec_arr.clip(min = 2, max = 6)
print ("Output clipped array : ", out_arr) 
```

**Output:**

```py
Input array :  [[(5.0, 2) (3.0, -4) (6.0, 9)]
 [(9.0, 1) (5.0, 4) (-12.0, -7)]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Output clipped array :  [[ 5\.  3\.  5.]
 [ 5\.  5\. -1.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output clipped array :  [[2 2 6]
 [2 4 2]]

```