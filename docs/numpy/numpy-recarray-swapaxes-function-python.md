# Numpy recarray.swapaxes()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-swapaxes-function-python/](https://www.geeksforgeeks.org/numpy-recarray-swapaxes-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.swapaxes()`** 函数返回 axis1 和 axis2 互换的数组视图。

> **语法:** `numpy.recarray.swapaxes(axis1, axis2)`
> 
> **参数:**
> **轴 1:**【int】第一轴。
> **轴 2:**【int】第二轴。
> 
> **返回:**【非数组】结果数组。

**代码#1 :**

```py
# Python program explaining
# numpy.recarray.swapaxes() method 

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

# applying recarray.swapaxes methods
# to float record array taking axis1 = 0 and axis2 = 1
out_arr = rec_arr.a.swapaxes(0, 1)
print ("Output float array : ", out_arr) 

# applying recarray.swapaxes methods 
# to int record array taking axis1 = 1 and axis2 = 0
out_arr = rec_arr.b.swapaxes(1, 0)
print ("Output int array : ", out_arr) 
```

**Output:**

```py
Input array :  [[(  5.,  2) (  3., -4) (  6.,  9)]
 [(  9.,  1) (  5.,  4) (-12., -7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output float array :  [[  5\.   9.]
 [  3\.   5.]
 [  6\. -12.]]
Output int array :  [[ 2  1]
 [-4  4]
 [ 9 -7]]

```

**代码#2 :**

我们将`numpy.recarray.swapaxes()`应用于整个记录数组。

```py
# Python program explaining
# numpy.recarray.swapaxes() method 

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

# applying recarray.swapaxes methods to 
# record array taking axis1 = 0 and axis2 = 1
out_arr = rec_arr.swapaxes(1, 0)

print ("Output record array : ", out_arr)
```

**Output:**

```py
Input array :  [[( 5.,  2) ( 3.,  4) ( 6., -7)]
 [( 9.,  1) ( 6.,  4) (-2., -7)]]
Output record array :  [[( 5.,  2) ( 9.,  1)]
 [( 3.,  4) ( 6.,  4)]
 [( 6., -7) (-2., -7)]]

```