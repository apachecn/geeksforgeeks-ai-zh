# Numpy recarray.compress()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-compress-function-python/](https://www.geeksforgeeks.org/numpy-recarray-compress-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.compress()`** 函数返回沿给定轴排列的选定切片。

> **语法:** `numpy.recarray.compress(condition, axis=None, out=None)`
> 
> **参数:**
> **条件:**【布尔一维数组】选择返回哪些条目的数组。
> **轴:**【int，可选】切片所沿的轴。
> **出:**结果会放在这个阵中。
> 
> **返回:** compressed_array，ndarray。

**代码#1 :**

```py
# Python program explaining
# numpy.recarray.compress() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, -4), (6.0, 9)], [(9.0, 1), (5.0, 4), (-12.0, -7)]],
        dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr)

# convert it to a record array, using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of int: ", rec_arr.b)

# applying recarray.compress methods to float record array
float_rec_arr = rec_arr.a
print("Record array of float: ", float_rec_arr)
out_arr = (rec_arr.a).compress([0, 1], axis = 0)
print ("Output compressed array : ", out_arr) 

# applying recarray.compress methods to int record array
int_rec_arr = rec_arr.b 
print("Record array of int: ", int_rec_arr)
out_arr = int_rec_arr.compress([True, False], axis = 1)
print ("Output compressed array : ", out_arr) 
```

**Output:**

```py
Input array :  [[(5.0, 2) (3.0, -4) (6.0, 9)]
 [(9.0, 1) (5.0, 4) (-12.0, -7)]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Output compressed array :  [[  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output compressed array :  [[2]
 [1]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.recarray.compress() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, -4), (6.0, 9)], [(9.0, 1), (5.0, 4), (-12.0, -7)]],
        dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr)

# convert it to a record array, using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of int: ", rec_arr.b)

# applying recarray.compress methods to whole record array
out_arr = rec_arr.compress([True, False], axis = 1)
print ("Output compressed array : ", out_arr) 
```

**Output:**

```py
Input array :  [[(5.0, 2) (3.0, -4) (6.0, 9)]
 [(9.0, 1) (5.0, 4) (-12.0, -7)]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output compressed array :  [[(5.0, 2)]
 [(9.0, 1)]]

```