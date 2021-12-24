# numpy.atleast_3d()用 Python

表示

> 原文:[https://www.geeksforgeeks.org/numpy-atleast_3d-in-python/](https://www.geeksforgeeks.org/numpy-atleast_3d-in-python/)

**`numpy.atleast_3d()`** 功能用于将输入转换为至少三维的数组。标量、一维和二维输入被转换为三维数组，而高维输入被保留。

输入包括标量、列表、元组列表、元组、元组元组元组、列表元组和数组。

> **语法:** numpy .至少 _ 3d(*数组)
> 
> **参数:**
> **arrays1，arrays2，…:**【array _ like】一个或多个数组样序列。非数组输入被转换为数组。已经具有三维或三维以上的数组将被保留。
> 
> **返回:**一个数组或数组列表，每个数组都有 arr.ndim > = 3。尽可能避免复制，并返回三维或三维以上的视图。例如，形状(N)的一维阵列变成形状(1，N，1)的视图，形状(M，N)的二维阵列变成形状(M，N，1)的视图。

**代码#1:工作**

```py
# Python program explaining
# numpy.atleast_3d() function

import numpy as geek
in_num = 10

print ("Input  number : ", in_num)

out_arr = geek.atleast_3d(in_num)
print ("output 3d array from input number : ", out_arr) 
```

**输出:**

```py
Input  number :  10
output 3d array from input number :  [[[10]]]

```

**代码#2:工作**

```py
# Python program explaining
# numpy.atleast_3d() function

import numpy as geek

my_list = [[2, 6, 10], 
          [8, 12, 16]]

print ("Input  list : ", my_list)

out_arr = geek.atleast_3d(my_list) 
print ("output array : ", out_arr) 
```

**输出:**

```py
Input  list :  [[2, 6, 10], [8, 12, 16]]
output array :  [[[ 2]
  [ 6]
  [10]]

 [[ 8]
  [12]
  [16]]]

```

**代码#3:工作**

```py
# Python program explaining
# numpy.atleast_3d() function
# when inputs are in high dimension

import numpy as geek

in_arr = geek.arange(16).reshape(1, 4, 4)
print ("Input  array :\n ", in_arr)

out_arr = geek.atleast_3d(in_arr)
print ("output  array :\n ", out_arr)
print(in_arr is out_arr)
```

**输出:**

```py
Input  array :
  [[[ 0  1  2  3]
  [ 4  5  6  7]
  [ 8  9 10 11]
  [12 13 14 15]]]
output  array :
  [[[ 0  1  2  3]
  [ 4  5  6  7]
  [ 8  9 10 11]
  [12 13 14 15]]]
True

```