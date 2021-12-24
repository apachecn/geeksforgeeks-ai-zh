# numpy 字符串运算| join()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-join-function/](https://www.geeksforgeeks.org/numpy-string-operations-join-function/)

`numpy.core.defchararray.join(sep, arr)`是 numpy 中做字符串运算的另一个函数。对于 arr 中的每个元素，它返回一个字符串的副本，其中数组的字符串元素已经由分隔符连接。

> **参数:**
> **sep :** 它用它们之间的字符串连接元素。
> **arr :** 输入数组。
> 
> **返回:**带有连接元素的字符串或 unicode 输出数组。

**代码#1 :**

```
# Python program explaining
# numpy.core.defchararray.join() method 

# importing numpy 
import numpy as geek

# input array 
in_arr = geek.array(['Python', 'Numpy', 'Pandas'])
print ("Input original array : ", in_arr) 

# creating the separator
sep = geek.array(['-', '+', '*'])

out_arr = geek.core.defchararray.join(sep, in_arr)
print ("Output joined array: ", out_arr) 
```

**Output:**

```
Input original array :  ['Python' 'Numpy' 'Pandas']
Output joined array:  ['P-y-t-h-o-n' 'N+u+m+p+y' 'P*a*n*d*a*s']

```