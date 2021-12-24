# Python 中的 numpy.left_shift()

> 原文:[https://www.geeksforgeeks.org/numpy-left_shift-in-python/](https://www.geeksforgeeks.org/numpy-left_shift-in-python/)

**`numpy.left_shift()`** 函数用于向左移动整数的位。

通过在 arr1 的右侧附加 arr 2 0(0)，这些位被向左移动。由于数字的内部表示是二进制格式，因此此操作相当于将 arr1 乘以 2**arr2。例如，如果数字是 5，我们想左移 2 位，那么左移 2 位后，结果将是 5*(2^2) = 20

> **语法:** numpy.left_shift(arr1，arr2，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，ufunc 'left_shift ')
> 
> **参数:**
> **arr1 :** 整数类型的数组 _ like
> **arr 2:**整数类型的数组 _ like
> 要追加到 arr1 的零的个数。arr2 的值应为正整数。
> 
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> 
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> 
> **返回:**整型数组。
> 返回 arr1，位左移 arr2 次。如果 arr1 和 arr2 都是标量，这就是标量。

**代码#1:工作**

```py
# Python program explaining
# left_shift() function

import numpy as geek
in_num = 5
bit_shift = 2

print ("Input  number : ", in_num)
print ("Number of bit shift : ", bit_shift ) 

out_num = geek.left_shift(in_num, bit_shift) 
print ("After left shifting 2 bit  : ", out_num) 
```

**输出:**

```py
Input  number :  5
Number of bit shift :  2
After left shifting 2 bit  :  20

```

**代码#2 :**

```py
# Python program explaining
# left_shift() function

import numpy as geek

in_arr = [2, 8, 15]
bit_shift =[3, 4, 5]

print ("Input array : ", in_arr) 
print ("Number of bit shift : ", bit_shift)

out_arr = geek.left_shift(in_arr, bit_shift) 
print ("Output array after left shifting: ", out_arr) 
```

**输出:**

```py
Input array :  [2, 8, 15]
Number of bit shift :  [3, 4, 5]
Output array after left shifting:  [ 16 128 480]

```