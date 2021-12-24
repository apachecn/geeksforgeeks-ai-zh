# numpy.atleast_1d()用 Python

表示

> 原文:[https://www.geeksforgeeks.org/numpy-atleast_1d-in-python/](https://www.geeksforgeeks.org/numpy-atleast_1d-in-python/)

**`numpy.atleast_1d()`** 函数在我们想要将输入转换为至少一维的数组时使用。标量输入被转换为一维数组，而高维输入被保留。

> **语法:** numpy .至少 _ 1d(*数组)
> 
> **参数:**
> **arrays1，arrays2，…:**【array _ like】一个或多个输入数组。
> 
> **返回:**【ndarray】一个数组或数组列表，每个数组都有一个 T2 = 1。只有在必要时才复印。

**代码#1:工作**

```
# Python program explaining
# numpy.atleast_1d() function

import numpy as geek
in_num = 10

print ("Input  number : ", in_num)

out_arr = geek.atleast_1d(in_num)
print ("output 1d array from input number : ", out_arr) 
```

**输出:**

```
Input  number :  10
output 1d array from input number :  [10]

```

**代码#2:工作**

```
# Python program explaining
# numpy.atleast_1d() function

import numpy as geek

my_list = [[2, 6, 10], 
          [8, 12, 16]]

print ("Input  list : ", my_list)

out_arr = geek.atleast_1d(my_list) 
print ("output array : ", out_arr) 
```

**输出:**

```
Input  list :  [[2, 6, 10], [8, 12, 16]]
output array :  [[ 2  6 10]
 [ 8 12 16]]

```

**代码#3:工作**

```
# Python program explaining
# numpy.atleast_1d() function
# when inputs are in high dimension

import numpy as geek

in_arr = geek.arange(9).reshape(3, 3)
print ("Input  array :\n ", in_arr)

out_arr = geek.atleast_1d(in_arr)
print ("output  array :\n ", out_arr)
print(in_arr is out_arr)
```

**输出:**

```
IInput  array :
  [[0 1 2]
 [3 4 5]
 [6 7 8]]
output  array :
  [[0 1 2]
 [3 4 5]
 [6 7 8]]
True'

```