# Numpy recarray.mean()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-mean-function-python/](https://www.geeksforgeeks.org/numpy-recarray-mean-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.mean()`** 函数返回给定轴上数组元素的平均值。

> **语法:** `numpy.recarray.mean(axis=None, dtype=None, out=None, keepdims=False)`
> 
> **参数:**
> **轴:**【无或 int 或 int 元组，可选】要沿其操作的一个或多个轴。默认情况下，使用展平输入。
> **数据类型:**【数据类型，可选】计算平均值时我们想要的类型。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **保持尺寸:**【布尔，可选】如果设置为真，则缩小的轴作为尺寸为 1 的尺寸留在结果中。
> 
> **返回:**【n 数组或标量】数组(如果轴为无，则为标量值)或具有沿指定轴的平均值的数组的算术平均值。

**代码#1 :**

```py
# Python program explaining
# numpy.recarray.mean() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, 6), (6.0, 10)],
                     [(9.0, 1), (5.0, 4), (-12.0, 7)]],
                     dtype =[('a', float), ('b', int)])

print ("Input array : ", in_arr)

# convert it to a record array,
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of float: ", rec_arr.a)
print("Record array of int: ", rec_arr.b)

# applying recarray.mean methods
# to float record array along default axis 
# i, e along flattened array
out_arr1 = rec_arr.a.mean()
# Mean of the flattened array 
print("\nMean of float record array, axis = None : ", out_arr1) 

# applying recarray.mean methods
# to float record array along axis 0
# i, e along vertical
out_arr2 = rec_arr.a.mean(axis = 0)
# Mean along 0 axis
print("\nMean of float record array, axis = 0 : ", out_arr2)

# applying recarray.mean methods
# to float record array along axis 1
# i, e along horizontal
out_arr3 = rec_arr.a.mean(axis = 1)
# Mean along 0 axis
print("\nMean of float record array, axis = 1 : ", out_arr3)

# applying recarray.mean methods
# to int record array along default axis 
# i, e along flattened array
out_arr4 = rec_arr.b.mean(dtype ='int')
# Mean of the flattened array 
print("\nMean of int record array, axis = None : ", out_arr4) 

# applying recarray.mean methods
# to int record array along axis 0
# i, e along vertical
out_arr5 = rec_arr.b.mean(axis = 0)
# Mean along 0 axis
print("\nMean of int record array, axis = 0 : ", out_arr5)

# applying recarray.mean methods
# to int record array along axis 1
# i, e along horizontal
out_arr6 = rec_arr.b.mean(axis = 1)
# Mean along 0 axis
print("\nMean of int record array, axis = 1 : ", out_arr6)
```

**Output:**

```py
Input array :  [[(  5.,  2) (  3.,  6) (  6., 10)]
 [(  9.,  1) (  5.,  4) (-12.,  7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2  6 10]
 [ 1  4  7]]

Mean of float record array, axis = None :  2.6666666666666665

Mean of float record array, axis = 0 :  [ 7\.  4\. -3.]

Mean of float record array, axis = 1 :  [4.66666667 0.66666667]

Mean of int record array, axis = None :  5

Mean of int record array, axis = 0 :  [1.5 5\.  8.5]

Mean of int record array, axis = 1 :  [6\. 4.]

```