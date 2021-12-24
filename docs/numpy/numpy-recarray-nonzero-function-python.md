# Numpy recarray .非零()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-非零-function-python/](https://www.geeksforgeeks.org/numpy-recarray-nonzero-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.nonzero()`** 函数用于获取记录数组中非零元素的索引。它返回一组数组，arr 的每个维度一个数组，包含该维度中非零元素的索引。

> **语法:** `numpy.recarray.nonzero()`
> 
> **参数:**无
> 
> **返回:**【数组的元组】非零元素的索引。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.nonzero() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(0.0, 2), (3.0, -4), (0.0, 9)],
                     [(9.0, 1), (5.0, 0), (-12.0, -7)]],
                     dtype =[('a', float), ('b', int)])

print ("Input array : ", in_arr)

# convert it to a record array,
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of float: ", rec_arr.a)
print("Record array of int: ", rec_arr.b)

# applying recarray.nonzero methods
# to float record array 
out_arr = rec_arr.a.nonzero()
print ("Indices of non zero elements : ", out_arr) 

# applying recarray.nonzero methods 
# to int record array
out_arr = rec_arr.b.nonzero()
print ("Indices of non zero elements : ", out_arr) 
```

**Output:**

> 输入数组:[[( 0。, 2) ( 3., -4) ( 0.，9)】
> 【(9。, 1) ( 5., 0) (-12.，-7)]
> 记录数组的 float: [[ 0。3.0.】
> 【9。5.-12.]
> 记录 int 的数组:[[ 2 -4 9]
> [ 1 0 -7]]
> 非零元素的索引:(数组([0，1，1，1]，dtype=int64)，数组([ 1，0，1，2]，dtype=int64))
> 非零元素的索引:(数组([0，0，0，1，1]，dtype=int64)，数组([0，1，2，0，2]，dtype=int64))

**代码#2 :**

我们将`numpy.recarray.nonzero()`应用于整个记录数组。

```
# Python program explaining
# numpy.recarray.nonzero() method 

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

# applying recarray.nonzero methods to record array
out_arr = rec_arr.nonzero()

print ("Output array : ", out_arr)
```

**Output:**

> 输入数组:[[( 5。, 2) ( 3., 4) ( 6.，-7)]
> [( 9。, 1) ( 6., 4) (-2.，-7)]
> 输出数组:(数组([0，0，0，1，1，1]，dtype=int64)，数组([0，1，2，0，1，2]，dtype=int64))