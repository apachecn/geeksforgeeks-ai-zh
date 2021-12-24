# num py recarray . cumber()函数| Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-reckler-cumber-function-python/

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.cumprod()`** 函数返回给定轴上数组元素的累计乘积。

> **语法:** `numpy.recarray.cumprod(axis=None, dtype=None, out=None)`
> 
> **参数:**
> **轴:**轴，累计乘积沿该轴计算。默认情况下，计算展平数组的乘积。
> **数据类型:**返回数组的类型，以及元素相乘的累加器的类型。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **Return :** 除非指定 out，否则将返回一个保存结果的新数组，在这种情况下，将返回该数组。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.cumprod() method 

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

# applying recarray.cumprod methods
# to float record array along axis 1
out_arr = rec_arr.a.cumprod( axis = 1)
print ("Output array along axis 1: ", out_arr) 

# applying recarray.cumprod methods 
# to int record array along axis 0
out_arr = rec_arr.b.cumprod(axis = 0)
print ("Output  array along axis 0: ", out_arr) 
```

**Output:**

```
Input array :  [[(  5.,  2) (  3., -4) (  6.,  9)]
 [(  9.,  1) (  5.,  4) (-12., -7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output array along axis 1:  [[   5\.   15\.   90.]
 [   9\.   45\. -540.]]
Output  array along axis 0:  [[  2  -4   9]
 [  2 -16 -63]]

```