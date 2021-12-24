# Numpy recarray.ptp()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-recarray-PTP-function-python/](https://www.geeksforgeeks.org/numpy-recarray-ptp-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.ptp()`** 函数返回沿给定轴的峰值到峰值(最大–最小)值。

> **语法:** `numpy.recarray.ptp(axis=None, out=None)`
> 
> **参数:**
> 
> **轴:**【int，可选】查找波峰的轴。默认情况下，展平阵列。
> **出:**【可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **返回:**【ndarray】保存结果的新数组，除非指定了 out，在这种情况下，将返回对 out 的引用。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.ptp() method 

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

# applying recarray.ptp methods
# to float record array along axis 1
out_arr = rec_arr.a.ptp( axis = 1)
print ("Output range array of float along axis 1: ", out_arr) 

# applying recarray.ptp methods
# to float record array along axis 0
out_arr = rec_arr.a.ptp( axis = 0)
print ("Output range array of float along axis 0: ", out_arr) 

# applying recarray.ptp methods
# to float record array along -1 axis 
out_arr = rec_arr.a.ptp( axis = -1)
print ("Output range array of float along -1 axis : ", out_arr) 

# applying recarray.ptp methods 
# to int record array along default axis value
out_arr = rec_arr.a.ptp()
print ("Output range of float array elements array along default axis: ", out_arr) 

# applying recarray.ptp methods
# to int record array along axis 1
out_arr = rec_arr.b.ptp( axis = 1)
print ("Output range array of int along axis 1: ", out_arr) 

# applying recarray.ptp methods
# to int record array along axis 0
out_arr = rec_arr.b.ptp( axis = 0)
print ("Output range array of int along axis 0: ", out_arr) 

# applying recarray.ptp methods
# to int record array along -1 axis 
out_arr = rec_arr.b.ptp( axis = -1)
print ("Output range array of int along -1 axis : ", out_arr) 

# applying recarray.ptp methods 
# to int record array along default axis value
out_arr = rec_arr.b.ptp()
print ("Output range of int array elements array along default axis: ", out_arr)  
```

**Output:**

```
Input array :  [[(  5.,  2) (  3., -4) (  6.,  9)]
 [(  9.,  1) (  5.,  4) (-12., -7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output range array of float along axis 1:  [ 3\. 21.]
Output range array of float along axis 0:  [ 4\.  2\. 18.]
Output range array of float along -1 axis :  [ 3\. 21.]
Output range of float array elements array along default axis:  21.0
Output range array of int along axis 1:  [13 11]
Output range array of int along axis 0:  [ 1  8 16]
Output range array of int along -1 axis :  [13 11]
Output range of int array elements array along default axis:  16

```