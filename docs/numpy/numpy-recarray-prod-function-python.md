# Numpy recarray.prod()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-prod-function-python/](https://www.geeksforgeeks.org/numpy-recarray-prod-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.prod()`** 函数返回给定轴上数组元素的乘积。

> **语法:** `numpy.recarray.prod(axis=None, dtype=None, out=None, keepdims=False)`
> 
> **参数:**
> **轴:**【无或整数或整数元组，可选】执行产品的一个或多个轴。默认值 axis=None 将计算输入数组中所有元素的乘积。如果轴为负，则从最后一个轴到第一个轴计数。
> **数据类型:**【数据类型，可选】返回数组的类型。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **保持尺寸:**【布尔，可选】如果设置为真，则缩小的轴作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据输入数组正确广播。
> 
> **返回:**【n 数组】给定轴上数组元素的乘积。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.prod() method 

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

# applying recarray.prod methods
# to float record array along axis 1
out_arr = rec_arr.a.prod( axis = 1)
print ("Output product array of float along axis 1: ", out_arr) 

# applying recarray.prod methods
# to float record array along axis 0
out_arr = rec_arr.a.prod( axis = 0)
print ("Output product array of float along axis 0: ", out_arr) 

# applying recarray.prod methods
# to float record array along -1 axis 
out_arr = rec_arr.a.prod( axis = -1)
print ("Output product array of float along -1 axis : ", out_arr) 

# applying recarray.prod methods 
# to int record array along default axis value
out_arr = rec_arr.b.prod()
print ("Output product of int array elements array along default axis: ", out_arr) 
```

**Output:**

```
Input array :  [[(  5.,  2) (  3., -4) (  6.,  9)]
 [(  9.,  1) (  5.,  4) (-12., -7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output product array of float along axis 1:  [  90\. -540.]
Output product array of float along axis 0:  [ 45\.  15\. -72.]
Output product array of float along -1 axis :  [  90\. -540.]
Output product of int array elements array along default axis:  2016

```