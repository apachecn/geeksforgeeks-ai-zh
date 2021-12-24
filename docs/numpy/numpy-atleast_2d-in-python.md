# numpy.atleast_2d()用 Python

表示

> 原文:[https://www.geeksforgeeks.org/numpy-atleast_2d-in-python/](https://www.geeksforgeeks.org/numpy-atleast_2d-in-python/)

**`numpy.atleast_2d()`** 函数用于将输入转换为至少二维的数组。标量和一维输入被转换成二维数组，而高维输入被保留。

> **语法:** numpy .至少 _ 2d(*数组)
> 
> **参数:**
> **arrays1，arrays2，…:**【array _ like】一个或多个数组样序列。非数组输入被转换为数组。已经具有两个或更多维度的数组将被保留。
> 
> **返回:**一个数组或数组列表，每个数组都有一个 T2 = 2。尽可能避免复制，并返回具有两个或更多维度的视图。

**代码#1:工作**

```
# Python program explaining
# numpy.atleast_2d() function

import numpy as geek
in_num = 10

print ("Input  number : ", in_num)

out_arr = geek.atleast_2d(in_num)
print ("output 2d array from input number : ", out_arr) 
```

**输出:**

```
Input  number :  10
output 2d array from input number :  [[10]]

```

**代码#2:工作**

```
# Python program explaining
# numpy.atleast_2d() function

import numpy as geek

my_list = [2, 6, 10], 

print ("Input  list : ", my_list)

out_arr = geek.atleast_2d(my_list) 
print ("output 2d  array : ", out_arr) 
```

**输出:**

```
Input  list :  ([2, 6, 10], )
output 2d  array :  [[ 2  6 10]]

```

**代码#3:工作**

```
# Python program explaining
# numpy.atleast_2d() function
# when inputs are in high dimension

import numpy as geek

in_arr = geek.arange(9).reshape(3, 3)
print ("Input  array :\n ", in_arr)

out_arr = geek.atleast_2d(in_arr)
print ("output  array :\n ", out_arr)
print(in_arr is out_arr)
```

**输出:**

```
Input  array :
  [[0 1 2]
 [3 4 5]
 [6 7 8]]
output  array :
  [[0 1 2]
 [3 4 5]
 [6 7 8]]
True

```