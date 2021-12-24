# Numpy recarray.min()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-min-function-python/](https://www.geeksforgeeks.org/numpy-recarray-min-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.min()`** 函数返回记录数组的最小值或沿一个轴的最小值。

> **语法:** `numpy.recarray.min(axis=None, out=None, keepdims=False)`
> 
> **参数:**
> **轴:**【无或 int 或 int 元组，可选】要沿其操作的一个或多个轴。默认情况下，使用展平输入。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **保持尺寸:**【布尔，可选】如果设置为真，则缩小的轴作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据输入数组正确广播。
> 
> **返回:**【数组或标量】记录数组的最小值。如果轴为“无”，则结果为标量值。如果给定轴，结果是一个 arr . ndim–1 维的数组。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.min() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, 4), (6.0, 8)],
                     [(9.0, 1), (5.0, 4), (-12.0, 7)]],
                     dtype =[('a', float), ('b', int)])

print ("Input array : ", in_arr)

# convert it to a record array,
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of float: ", rec_arr.a)
print("Record array of int: ", rec_arr.b)

# applying recarray.min methods
# to float record array along default axis 
# i, e along flattened array
out_arr1 = rec_arr.a.min()
# Minimum of the flattened array 
print("\nMin of float record array, axis = None : ", out_arr1) 

# applying recarray.min methods
# to float record array along axis 0
# i, e along vertical
out_arr2 = rec_arr.a.min(axis = 0)
# Minimum along 0 axis
print("\nMin of float record array, axis = 0 : ", out_arr2)

# applying recarray.min methods
# to float record array along axis 1
# i, e along horizontal
out_arr3 = rec_arr.a.min(axis = 1)
# Minimum along 0 axis
print("\nMin of float record array, axis = 1 : ", out_arr3)

# applying recarray.min methods
# to int record array along default axis 
# i, e along flattened array
out_arr4 = rec_arr.b.min()
# Minimum of the flattened array 
print("\nMin of int record array, axis = None : ", out_arr4) 

# applying recarray.min methods
# to int record array along axis 0
# i, e along vertical
out_arr5 = rec_arr.b.min(axis = 0)
# Minimum along 0 axis
print("\nMin of int record array, axis = 0 : ", out_arr5)

# applying recarray.min methods
# to int record array along axis 1
# i, e along horizontal
out_arr6 = rec_arr.b.min(axis = 1)
# Minimum along 0 axis
print("\nMin of int record array, axis = 1 : ", out_arr6)
```

**Output:**

```
Input array :  [[(  5., 2) (  3., 4) (  6., 8)]
 [(  9., 1) (  5., 4) (-12., 7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[2 4 8]
 [1 4 7]]

Min of float record array, axis = None :  -12.0

Min of float record array, axis = 0 :  [  5\.   3\. -12.]

Min of float record array, axis = 1 :  [  3\. -12.]

Min of int record array, axis = None :  1

Min of int record array, axis = 0 :  [1 4 7]

Min of int record array, axis = 1 :  [2 1]

```