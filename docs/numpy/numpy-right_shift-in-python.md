# Python 中的 numpy.right_shift()

> 原文:[https://www.geeksforgeeks.org/numpy-right_shift-in-python/](https://www.geeksforgeeks.org/numpy-right_shift-in-python/)

**`numpy.right_shift()`** 函数用于向右移动整数的位。

因为数字的内部表示是二进制格式，所以这个操作相当于将 arr1 除以 2**arr2。例如，如果数字是 20，我们想要右移 2 位，那么在右移 2 位之后，结果将是 20/(2^2) = 5。

> **语法:** numpy.right_shift(arr1，arr2，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，ufunc 'right_shift ')
> 
> **参数:**
> **arr1 :** 整型数组 _ like
> **arr 2:**整型数组 _ like
> arr 1 右侧需要去掉的位数。
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
> 返回 arr1，位向右移动 arr2 次。如果 arr1 和 arr2 都是标量，这就是标量。

**代码#1:工作**

```
# Python program explaining
# right_shift() function

import numpy as geek
in_num = 20
bit_shift = 2

print ("Input  number : ", in_num)
print ("Number of bit shift : ", bit_shift ) 

out_num = geek.right_shift(in_num, bit_shift) 
print ("After right shifting 2 bit  : ", out_num) 
```

**输出:**

```
Input  number :  20
Number of bit shift :  2
After right shifting 2 bit  :  5

```

**代码#2 :**

```
# Python program explaining
# right_shift() function

import numpy as geek

in_arr = [24, 48, 16]
bit_shift =[3, 4, 2]

print ("Input array : ", in_arr) 
print ("Number of bit shift : ", bit_shift)

out_arr = geek.right_shift(in_arr, bit_shift) 
print ("Output array after right shifting: ", out_arr) 
```

**输出:**

```
Input array :  [24, 48, 16]
Number of bit shift :  [3, 4, 2]
Output array after right shifting:  [3 3 4]

```