# Numpy recarray.ravel()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-recarray-ravel-function-python/](https://www.geeksforgeeks.org/numpy-recarray-ravel-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.ravel()`** 函数返回连续的扁平记录数组，即包含所有输入数组元素且类型相同的 1D 数组。

> **语法:** `numpy.recarray.ravel([order])`
> 
> **参数:**
> 
> **顺序:** ['C '，' F '，' A '，' K '，可选]
> 
> *   “C”是指以行为主的 C 风格顺序对元素进行索引，最后一个轴索引变化最快，回到第一个轴索引变化最慢。
> *   “f”是指以主要列、Fortran 风格的顺序对元素进行索引，第一个索引变化最快，最后一个索引变化最慢。
> *   “a”表示以类似 Fortran 的索引顺序读取元素，如果 a 在内存中是 Fortran 连续的，则以类似 C 的顺序读取。
> *   “k”是指按照元素在内存中出现的顺序读取元素，除非当步长为负时反转数据。
> 
> 默认情况下，使用“C”索引顺序。
> 
> **返回:**【类似数组】扁平数组，与输入数组具有相同的类型，并根据选择进行排序。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.ravel() method 

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

# applying recarray.ravel methods
# to float record array 
out_arr = rec_arr.a.ravel()
print ("Output flattenrd float array : ", out_arr) 

# applying recarray.ravel methods
# to int record array 
out_arr = rec_arr.b.ravel()
print ("Output flattenrd int array : ", out_arr) 
```

**Output:**

```
Input array :  [[(  5.,  2) (  3., -4) (  6.,  9)]
 [(  9.,  1) (  5.,  4) (-12., -7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output flattenrd float array :  [  5\.   3\.   6\.   9\.   5\. -12.]
Output flattenrd int array :  [ 2 -4  9  1  4 -7]

```

**代码#2 :**

我们将`numpy.recarray.ravel()`应用于整个记录数组。

```
# Python program explaining
# numpy.recarray.ravel() method 

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

# applying recarray.ravel methods to  record array
out_arr = rec_arr.ravel()

print ("Output array : ", out_arr)
```

**Output:**

```
Input array :  [[( 5.,  2) ( 3.,  4) ( 6., -7)]
 [( 9.,  1) ( 6.,  4) (-2., -7)]]
Output array :  [( 5.,  2) ( 3.,  4) ( 6., -7) ( 9.,  1) ( 6.,  4) (-2., -7)]

```