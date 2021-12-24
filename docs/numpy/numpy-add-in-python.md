# Python 中的 numpy.add()

> 原文:[https://www.geeksforgeeks.org/numpy-add-in-python/](https://www.geeksforgeeks.org/numpy-add-in-python/)

**`numpy.add()`** 功能是在我们要计算两个数组的相加时使用的。它按元素添加参数。如果两个阵列的形状不相同，即`arr1.shape != arr2.shape`，则它们必须可宽铸为一个共同的形状(可以是一个或另一个的形状)。

> **语法:** numpy.add(arr1，arr2，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，subok=True[，signature，extobj]，ufunc 'add ')
> 
> **参数:**
> **arr 1:**【array _ like 或标量】输入数组。
> **arr 2:**【array _ like 或标量】输入数组。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **其中:**【array _ like，可选】值为 True 表示计算该位置的 ufunc，值为 False 表示将该值单独留在输出中。
> ****kwargs :** 允许将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时使用。
> 
> **返回:**【数组或标量】arr1 和 arr2 的和，元素方式。如果 arr1 和 arr2 都是标量，则返回标量。

**代码#1:工作**

```
# Python program explaining
# numpy.add() function
# when inputs are scalar

import numpy as geek
in_num1 = 10
in_num2 = 15

print ("1st Input  number : ", in_num1)
print ("2nd Input  number : ", in_num2)

out_num = geek.add(in_num1, in_num2) 
print ("output number after addition  : ", out_num) 
```

**输出:**

```
1st Input  number :  10
2nd Input  number :  15
output number after addition  :  25

```

**代码#2 :**

```
# Python program explaining
# numpy.add() function
# when inputs are array

import numpy as geek

in_arr1 = geek.array([[2, -7, 5], [-6, 2, 0]])
in_arr2 = geek.array([[5, 8, -5], [3, 6, 9]])

print ("1st Input array : ", in_arr1) 
print ("2nd Input array : ", in_arr2) 

out_arr = geek.add(in_arr1, in_arr2) 
print ("output added array : ", out_arr) 
```

**输出:**

```
1st Input array :  [[ 2 -7  5]
 [-6  2  0]]
2nd Input array :  [[ 5  8 -5]
 [ 3  6  9]]
output added array :  [[ 7  1  0]
 [-3  8  9]]

```