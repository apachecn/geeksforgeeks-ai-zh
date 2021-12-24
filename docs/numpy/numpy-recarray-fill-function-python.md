# Numpy recarray.fill()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-fill-function-python/](https://www.geeksforgeeks.org/numpy-recarray-fill-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.fill()`** 函数用标量值填充记录数组。

> **语法:** `numpy.recarray.fill(value)`
> 
> **参数:**
> **值:**【标量】数组的所有元素都会被赋予这个值。
> 
> **返回:**输出数组充满值。

**代码#1 :**

```py
# Python program explaining
# numpy.recarray.fill() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([(5.0, 2), (3.0, -4), (6.0, 9),],
                     dtype =[('a', float), ('b', int)])

print ("Input array : ", in_arr)

# convert it to a record array,
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of float: ", rec_arr.a)
print("Record array of int: ", rec_arr.b)

# applying recarray.fill methods
# to float record array 
rec_arr.a.fill(5)
print ("Output filled array : ", rec_arr.a) 

# applying recarray.fill methods 
# to int record array 
rec_arr.b.fill(0)
print ("Output filled array : ", rec_arr.b) 
```

**Output:**

```py
Input array :  [(5.,  2) (3., -4) (6.,  9)]
Record array of float:  [5\. 3\. 6.]
Record array of int:  [ 2 -4  9]
Output filled array :  [5\. 5\. 5.]
Output filled array :  [0 0 0]

```

**代码#2 :**

我们将`numpy.recarray.fill()`应用于整个记录数组。

```py
# Python program explaining
# numpy.recarray.fill() method 

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

# applying recarray.fill methods to  record array
rec_arr.fill(0)

print ("Output filled array : ", rec_arr)
```

**Output:**

```py
Input array :  [[( 5.,  2) ( 3.,  4) ( 6., -7)]
 [( 9.,  1) ( 6.,  4) (-2., -7)]]
Output filled array :  [[(0., 0) (0., 0) (0., 0)]
 [(0., 0) (0., 0) (0., 0)]]

```