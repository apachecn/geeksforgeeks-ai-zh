# Python 中的 numpy.array_str()

> 原文:[https://www.geeksforgeeks.org/numpy-array_str-in-python/](https://www.geeksforgeeks.org/numpy-array_str-in-python/)

**`numpy.array_str()`** 函数用于将数组中的数据表示为字符串。

数组中的数据作为单个字符串返回。该函数类似于 array_repr，不同之处在于 array_repr 还返回关于数组类型及其数据类型的信息。

> **语法:** numpy.array_str(arr，max _ line _ width =无，precision =无，suppress _ small =无)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **最大线宽:**【int，可选】如果文本比最大线宽长，插入新行。默认为，间接的，75。
> **精度:**【int，可选】浮点精度。默认为当前打印精度(一般为 8)。
> **supprest _ small:**【bool，可选】它将非常小的数字表示为零，默认为 False。非常小的数字由精度定义，如果精度为 8，则小于 5e-9 的数字表示为零。
> 
> **返回:**【str】数组的字符串表示形式。

**代码#1:工作**

```
# Python program explaining
# array_str() function

import numpy as geek
arr = geek.array([4, -8, 7 ])

print ("Input  array : ", arr)
print(type(arr))

out_arr = geek.array_str(arr)
print ("The string representation of input array : ", out_arr) 
print(type(out_arr))
```

**输出:**

```
Input  array :  [ 4 -8  7]
class 'numpy.ndarray'
The string representation of input array :  array([ 4, -8,  7])
class 'str'

```

**代码#2:工作**

```
# Python program explaining
# array_str() function

import numpy as geek
in_arr = geek.array([5e-8, 4e-7, 8, -4])

print ("Input  array : ", in_arr)
print(type(in_arr))

out_arr = geek.array_str(in_arr, precision = 6, suppress_small = True)
print ("The string representation of input array : ", out_arr) 
print(type(out_arr))
```

**输出:**

```
Input  array :  [  5.00000000e-08   4.00000000e-07   8.00000000e+00  -4.00000000e+00]
class 'numpy.ndarray'
The string representation of input array :  array([ 0.,  0.,  8., -4.])
class 'str'

```