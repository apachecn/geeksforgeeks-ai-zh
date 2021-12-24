# Numpy recarray .共轭()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-共轭-函数-python/](https://www.geeksforgeeks.org/numpy-recarray-conjugate-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.conjugate()`** 函数通过共轭数组中的复数返回一个数组。

> **语法:** `numpy.recarray.conjugate(out=None)`
> 
> **参数:**
> 
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **返回:**输出数组与输入数组具有相同的维度，与结果一起放置。

**代码#1 :**

```py
# Python program explaining
# numpy.recarray.conjugate() method 

# importing numpy as geek
import numpy as geek

# creating input array 
in_arr = geek.array([[(4.0 + 1j, 1 + 3j), (5.0, 5-1j),
                      (8.0-6j, 9)], [(9.0, 1), 
                     (7.0 + 1j, 3-1j), (-2.0 + 6j, -7 + 3j)]],
                     dtype =[('a', complex), ('b', complex)])

print ("Input array : ", in_arr)

# convert it to a record array, using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)

# 1st record array
print("1st Record array of complex : ", rec_arr.a)
# applying recarray.conjugate methods to 1st record array
out_arr = (rec_arr.a).conjugate()
print ("Output 1st conjugated array : ", out_arr) 

# 2nd record array
rec_arr = rec_arr.b
print("2nd Record array of complex : ", rec_arr)

# applying recarray.conjugate methods to 2nd record array
out_arr = rec_arr.conjugate()
print ("Output 2nd conjugated array : ", out_arr) 
```

**Output:**

```py
Input array :  [[( 4.+1.j,  1.+3.j) ( 5.+0.j,  5.-1.j) ( 8.-6.j,  9.+0.j)]
 [( 9.+0.j,  1.+0.j) ( 7.+1.j,  3.-1.j) (-2.+6.j, -7.+3.j)]]
1st Record array of complex :  [[ 4.+1.j  5.+0.j  8.-6.j]
 [ 9.+0.j  7.+1.j -2.+6.j]]
Output 1st conjugated array :  [[ 4.-1.j  5.-0.j  8.+6.j]
 [ 9.-0.j  7.-1.j -2.-6.j]]
2nd Record array of complex :  [[ 1.+3.j  5.-1.j  9.+0.j]
 [ 1.+0.j  3.-1.j -7.+3.j]]
Output 2nd conjugated array :  [[ 1.-3.j  5.+1.j  9.-0.j]
 [ 1.-0.j  3.+1.j -7.-3.j]]

```