# Numpy recarray.trace()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-trace-function-python/](https://www.geeksforgeeks.org/numpy-recarray-trace-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.trace()`** 函数用于返回沿数组对角线的和。

> **语法:** `numpy.recarray.trace(offset=0, axis1=0, axis2=1, dtype=None, out=None)`
> 
> **参数:**
> **偏移:**【int，可选】对角线与主对角线的偏移。可以是积极的也可以是消极的。默认为 0。
> **轴 1:**【int，可选】用作二维子阵列的第一轴和第二轴的轴，对角线应取自该轴。
> **轴 2:**【int，可选】用作二维子阵列的第一轴和第二轴的轴，对角线应取自该轴。
> **数据类型:**【可选】确定返回数组的数据类型。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **返回:**【ndarray】记录数组对角线元素的和。

**代码#1 :**

```py
# Python program explaining
# numpy.recarray.trace() method 

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

# applying recarray.trace methods
# to float record array 
out_arr = rec_arr.a.trace()
print ("Output float traced array : ", out_arr) 

# applying recarray.trace methods 
# to int record array
out_arr = rec_arr.b.trace()
print ("Output int traced array : ", out_arr) 
```

**Output:**

```py
Input array :  [[(  5.,  2) (  3., -4) (  6.,  9)]
 [(  9.,  1) (  5.,  4) (-12., -7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output float traced array :  10.0
Output int traced array :  6

```