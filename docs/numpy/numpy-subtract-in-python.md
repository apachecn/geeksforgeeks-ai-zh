# Python 中的 numpy .减法()

> 原文:[https://www.geeksforgeeks.org/numpy-subtract-in-python/](https://www.geeksforgeeks.org/numpy-subtract-in-python/)

**`numpy.subtract()`** 函数是我们想要计算两个数组的差时使用的。它按元素返回 arr1 和 arr2 的差值。

> **语法:** numpy .减法(arr1，arr2，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，subok=True[，signature，extobj]，ufunc '减法')
> 
> **参数:**
> **arr 1:**【array _ like 或标量】第一输入数组。
> **arr2 :** 【类数组或标量】第二输入数组。
> **dtype :** 返回数组的类型。默认情况下，使用 arr 的*数据类型*。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **其中:**【array _ like，可选】值为 True 表示计算该位置的 ufunc，值为 False 表示将该值单独留在输出中。
> ****kwargs :** 允许将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时使用。
> 
> **返回:**【数组或标量】arr1 和 arr2 的差，元素方式。如果 arr1 和 arr2 都是标量，则返回标量。

**代码#1 :**

```py
# Python program explaining
# numpy.subtract() function

import numpy as geek
in_num1 = 4
in_num2 = 6

print ("1st Input  number : ", in_num1)
print ("2nd Input  number : ", in_num2)

out_num = geek.subtract(in_num1, in_num2) 
print ("Difference of two input number : ", out_num) 
```

**Output :**

```py
1st Input number :  4
2nd Input number :  6
Difference of two input number :  -2

```

**代码#2 :**

```py
# Python program explaining
# numpy.subtract() function

import numpy as geek

in_arr1 = geek.array([[2, -4, 5], [-6, 2, 0]])
in_arr2 = geek.array([[0, -7, 5], [5, -2, 9]])

print ("1st Input array : ", in_arr1)
print ("2nd Input array : ", in_arr2)

out_arr = geek.subtract(in_arr1, in_arr2) 
print ("Output array: ", out_arr) 
```

**Output :**

```py
1st Input array :  [[ 2 -4  5]
 [-6  2  0]]
2nd Input array :  [[ 0 -7  5]
 [ 5 -2  9]]
Output array:  [[  2   3   0]
 [-11   4  -9]]

```