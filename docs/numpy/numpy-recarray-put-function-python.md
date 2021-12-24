# Numpy recarray.put()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-put-function-python/](https://www.geeksforgeeks.org/numpy-recarray-put-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.put()`** 函数用给定的值替换记录数组的特定元素。索引在展平的目标数组上工作。

> **语法:** `numpy.recarray.put(indices, values, mode='raise')`
> 
> **参数:**
> **指数:**【array _ like】目标指数，解释为整数。
> **值:**【array _ like】放置在 at 目标指数中的值。如果值比 ind 短，将根据需要重复。
> **模式:** ['提升'，'环绕'，'剪辑'，可选]指定越界索引的行为方式。
> 
> **返回:**【非数组】结果数组。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.put() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([(1.0, 2), (3.0, -4), (5.0, 6),
                     (7.0, 8), (9.0, -4), (11.0, -2)],
                     dtype =[('a', float), ('b', int)])

print ("Input array : ", in_arr)

# convert it to a record array,
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of float: ", rec_arr.a)
print("Record array of int: ", rec_arr.b)

# applying recarray.put methods
# to float record array in default mode
rec_arr.a.put( [0, 2], [-14, 15])
print ("Output float array in default mode : ", rec_arr.a) 

# applying recarray.put methods
# to float record array in clip mode
rec_arr.a.put( 13, -4, mode ='clip')
print ("Output  float array in clip mode : ", rec_arr.a) 

# applying recarray.put methods 
# to int record array 
rec_arr.b.put([1, 2, 4], [10, 15, 20])
print ("Output int array in default mode : ", rec_arr.b) 

# applying recarray.put methods
# to int record array in clip mode
rec_arr.b.put(8, 100, mode ='clip')
print ("Output  int array in clip mode : ", rec_arr.b) 
```

**Output:**

```
Input array :  [( 1.,  2) ( 3., -4) ( 5.,  6) ( 7.,  8) ( 9., -4) (11., -2)]
Record array of float:  [ 1\.  3\.  5\.  7\.  9\. 11.]
Record array of int:  [ 2 -4  6  8 -4 -2]
Output float array in default mode :  [-14\.   3\.  15\.   7\.   9\.  11.]
Output  float array in clip mode :  [-14\.   3\.  15\.   7\.   9\.  -4.]
Output int array in default mode :  [ 2 10 15  8 20 -2]
Output  int array in clip mode :  [  2  10  15   8  20 100]

```