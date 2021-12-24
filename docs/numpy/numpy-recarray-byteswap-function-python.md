# Numpy recarray.byteswap()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-recarray-bytes WAP-function-python/](https://www.geeksforgeeks.org/numpy-recarray-byteswap-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.byteswap()`** 函数交换数组元素的字节。

> **语法:** `numpy.recarray.byteswap(inplace=False)`
> 
> **参数:**
> **在位:**【bool，可选】如果为真，就地交换字节，默认为假。
> 
> **返回:**【n 数组】字节数组。如果在某个地方是真的，这就是对自己的看法。

**代码:**

```
# Python program explaining
# numpy.recarray.byteswap() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([(5.0, 2), (3.0, -4), (6.0, 9)],
                    dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr)

# convert it to a record array, 
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)

# applying recarray.byteswap methods to record array 
out_arr = rec_arr.byteswap()
print ("Output swapped  record array : ", out_arr) 
```

**Output:**

```
Input array :  [(5.0, 2) (3.0, -4) (6.0, 9)]
Output swapped  record array :  [(2.561e-320, 144115188075855872) (1.0435e-320, -216172782113783809)
 (3.067e-320, 648518346341351424)]

```