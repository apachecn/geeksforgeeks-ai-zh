# Python 中的 numpy.negative()

> 原文:[https://www.geeksforgeeks.org/numpy-negative-in-python/](https://www.geeksforgeeks.org/numpy-negative-in-python/)

**`numpy.negative()`** 函数是在我们要计算数组元素的负数时使用的。它返回数组的元素负值或标量的负值。

> **语法:** numpy.negative(arr，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，subok=True[，signature，extobj]，ufunc 'negative ')
> 
> **参数:**
> **arr:**【array _ like 或标量】输入数组。
> **dtype :** 返回数组的类型。默认情况下，使用 arr 的*数据类型*。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **其中:**【array _ like，可选】值为 True 表示计算该位置的 ufunc，值为 False 表示将该值单独留在输出中。
> ****kwargs :** 允许将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时使用。
> 
> **返回:**【数组或标量】返回的数组或标量= -(输入 arr 或标量)

**代码#1:工作**

```
# Python program explaining
# numpy.negative() function

import numpy as geek
in_num = 10

print ("Input  number : ", in_num)

out_num = geek.negative(in_num) 
print ("negative of input number : ", out_num) 
```

**输出:**

```
Input  number :  10
negative of input number :  -10

```

**代码#2 :**

```
# Python program explaining
# numpy.negative function

import numpy as geek

in_arr = geek.array([[2, -7, 5], [-6, 2, 0]])

print ("Input array : ", in_arr) 

out_arr = geek.negative(in_arr) 
print ("negative of array elements: ", out_arr) 
```

**输出:**

```
Input array :  [[  2\.   2\.   2.]
 [  2\.   2\.  nan]]
product of array elements:  32.0Input array :  [[ 2 -7  5]
 [-6  2  0]]
negative of array elements:  [[-2  7 -5]
 [ 6 -2  0]]

```