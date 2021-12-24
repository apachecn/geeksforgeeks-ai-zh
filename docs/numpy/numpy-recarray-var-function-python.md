# Numpy recarray.var()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-var-function-python/](https://www.geeksforgeeks.org/numpy-recarray-var-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.var()`** 函数返回数组元素沿给定轴的方差。

> **语法:** `numpy.recarray.var(axis=None, dtype=None, out=None, ddof=0, keepdims=False)`
> 
> **参数:**
> **轴:**【int 或 int 的元组】轴，我们要沿着该轴计算方差。否则，它将考虑将 arr 展平(在所有轴上工作)。axis = 0 表示沿列的方差，axis = 1 表示沿行的方差。
> **数据类型:**【数据类型，可选】计算方差时我们想要的类型。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **ddof:**【int，可选】Delta 自由度”:计算中使用的除数为 N–ddof，其中 N 代表元素个数。默认情况下，ddof 为零。
> **保持尺寸:**【布尔，可选】如果设置为真，减少的轴将作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据输入数组正确广播。
> 
> **返回:**【ndarray】如果 out=None，则返回包含方差的新数组；否则，将返回对输出数组的引用。

**代码#1 :**

```py
# Python program explaining
# numpy.recarray.var() method 

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

# applying recarray.var methods
# to float record array along axis 1
out_arr = rec_arr.a.var(axis = 1)
print ("Output array containing variance along axis 1: ", out_arr) 

# applying recarray.var methods
# to float record array along axis 0
out_arr = rec_arr.a.var(axis = 0)
print ("Output array containing variance along axis 0: ", out_arr) 

# applying recarray.var methods
# to float record array along default axis
out_arr = rec_arr.a.var()
print ("Output array containing variance along default axis : ", out_arr) 

# applying recarray.var methods
# to int record array along axis 1
out_arr = rec_arr.b.var(axis = 1)
print ("Output array containing variance along axis 1: ", out_arr) 

# applying recarray.var methods
# to int record array along axis 0
out_arr = rec_arr.b.var(axis = 0)
print ("Output array containing variance along axis 0: ", out_arr) 

# applying recarray.var methods
# to int record array along default axis
out_arr = rec_arr.b.var()
print ("Output array containing variance along default axis : ", out_arr) 
```

**Output:**

```py
Input array :  [[(  5.,  2) (  3., -4) (  6.,  9)]
 [(  9.,  1) (  5.,  4) (-12., -7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output array containing variance along axis 1:  [ 1.55555556 82.88888889]
Output array containing variance along axis 0:  [ 4\.  1\. 81.]
Output array containing variance along default axis :  46.22222222222222
Output array containing variance along axis 1:  [28.22222222 21.55555556]
Output array containing variance along axis 0:  [ 0.25 16\.   64\.  ]
Output array containing variance along default axis :  27.138888888888882

```