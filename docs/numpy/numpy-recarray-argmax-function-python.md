# Numpy recarray.argmax()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-recarray-arg max-function-python/](https://www.geeksforgeeks.org/numpy-recarray-argmax-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.argmax()`** 函数返回数组中最大元素在特定轴上的索引。

> **语法:** `numpy.recarray.argmax(axis=None, out=None)`
> 
> **参数:**
> **轴:**【int，可选】沿指定轴如 0 或 1
> **出:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **返回:**【整数数组】数组中的索引，其形状与数组相同。沿轴的尺寸被移除的形状。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.argmax() method 

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
print("Record array of float: ", rec_arr.a)
print("Record array of int: ", rec_arr.b)

# applying recarray.argmax methods to
# float record array along axis 1
out_arr = geek.recarray.argmax(rec_arr.a, axis = 1)
print ("Output array along axis 1: ", out_arr) 

# applying recarray.argmax methods to
# int record array along axis 0
out_arr = geek.recarray.argmax(rec_arr.b, axis = 0)
print ("Output array along axis 0: ", out_arr) 
```

**Output:**

```
Input array :  [[(5.0, 2) (3.0, 4) (6.0, -7)]
 [(9.0, 1) (6.0, 4) (-2.0, -7)]]
Record array of float:  [[ 5\.  3\.  6.]
 [ 9\.  6\. -2.]]
Record array of int:  [[ 2  4 -7]
 [ 1  4 -7]]
Output array along axis 1:  [2 0]
Output array along axis 0:  [0 0 0]

```

**代码#2 :**

如果我们将`numpy.recarray.argmax()`应用于整个记录数组，那么它将给出`Type error`。

```
# Python program explaining
# numpy.recarray.argmax() method 
# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, 4), (6.0, -7)],
                     [(9.0, 1), (6.0, 4), (-2.0, -7)]],
                     dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr)

# convert it to a record array, using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)

# applying recarray.argmax methods to  record array
out_arr = geek.recarray.argmax(rec_arr)
```

**Output:**

> TypeError:无法根据规则“safe”将数组数据从 dtype(((numpy . record，[('a '，' < f8 ')，(' b '，' < i8 ')))强制转换为 dtype('V16 ')