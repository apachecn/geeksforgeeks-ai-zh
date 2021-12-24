# Numpy recarray.tolist()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-to list-function-python/](https://www.geeksforgeeks.org/numpy-recarray-tolist-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.tolist()`** 函数用于使数组成为一个(可能是嵌套的)列表。它以(嵌套的)Python 列表的形式返回数组数据的副本。数据项被转换为最近的兼容 Python 类型。

> **语法:** `numpy.recarray.tolist()`
> 
> **参数:**T2**无**
> 
> **返回:**【列表】数组元素可能嵌套的列表。

**代码#1 :**

```py
# Python program explaining
# numpy.recarray.tolist() method 

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

# applying recarray.tolist methods
# to float record array 
out_arr = rec_arr.a.tolist()
print ("Output list of float record array  ", out_arr) 

# applying recarray.tolist methods 
# to int record array 
out_arr = rec_arr.b.tolist()
print ("Output list of int record array ", out_arr) 
```

**Output:**

```py
Input array :  [[(  5.,  2) (  3., -4) (  6.,  9)]
 [(  9.,  1) (  5.,  4) (-12., -7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output list of float record array   [[5.0, 3.0, 6.0], [9.0, 5.0, -12.0]]
Output list of int record array  [[2, -4, 9], [1, 4, -7]]

```

**代码#2 :**

我们将`numpy.recarray.tolist()`应用于整个记录数组。

```py
# Python program explaining
# numpy.recarray.tolist() method 

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

# applying recarray.tolist methods to  
# record array in default order
out_arr = rec_arr.tolist()
print ("Output list of record array  ", out_arr) 
```

**Output:**

```py
Input array :  [[( 5.,  2) ( 3.,  4) ( 6., -7)]
 [( 9.,  1) ( 6.,  4) (-2., -7)]]
Output list of record array   [[(5.0, 2), (3.0, 4), (6.0, -7)], [(9.0, 1), (6.0, 4), (-2.0, -7)]]

```