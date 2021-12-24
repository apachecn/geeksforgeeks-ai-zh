# Python 中的 numpy.array_repr()

> 原文:[https://www.geeksforgeeks.org/numpy-array_repr-in-python/](https://www.geeksforgeeks.org/numpy-array_repr-in-python/)

**`numpy.array_repr()`** 函数用于将数组转换为字符串。

> **语法:** numpy.array_repr(arr，max _ line _ width =无，precision =无，suppress _ small =无)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **max _ line _ width:**【int，可选】字符串应跨越的最大列数。换行符在数组元素后适当地拆分字符串。
> **精度:**【int，可选】浮点精度。默认为当前打印精度(一般为 8)。
> **supprest _ small:**【bool，可选】它将非常小的数字表示为零，默认为 False。非常小的数字由精度定义，如果精度为 8，则小于 5e-9 的数字表示为零。
> 
> **返回:**【str】数组的字符串表示形式。

**代码#1:工作**

```py
# Python program explaining
# array_repr() function

import numpy as geek
arr = geek.array([4, -8, 7 ])

print ("Input  array : ", arr)
print(type(arr))

out_arr = geek.array_repr(arr)
print ("The string representation of input array : ", out_arr) 
print(type(out_arr))
```

**输出:**

```py
Input  array :  [ 4 -8  7]
class 'numpy.ndarray'
The string representation of input array :  array([ 4, -8,  7])
class 'str'

```

**代码#2:工作**

```py
# Python program explaining
# array_repr() function

import numpy as geek
in_arr = geek.array([5e-8, 4e-7, 8, -4])

print ("Input  array : ", in_arr)
print(type(in_arr))

out_arr = geek.array_repr(in_arr, precision = 6, suppress_small = True)
print ("The string representation of input array : ", out_arr) 
print(type(out_arr))
```

**输出:**

```py
Input  array :  [  5.00000000e-08   4.00000000e-07   8.00000000e+00  -4.00000000e+00]
class 'numpy.ndarray'
The string representation of input array :  array([ 0.,  0.,  8., -4.])
class 'str'

```