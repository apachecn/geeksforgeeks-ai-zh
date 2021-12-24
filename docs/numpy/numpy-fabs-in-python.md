# Python 中的 numpy.fabs()

> 原文:[https://www.geeksforgeeks.org/numpy-fabs-in-python/](https://www.geeksforgeeks.org/numpy-fabs-in-python/)

**`numpy.fabs()`** 函数用于逐元素计算绝对值。该函数返回 arr 中数据的绝对值(正幅度)。它总是以浮点形式返回绝对值。

> **语法:** numpy.fabs(arr，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，ufunc 'fabs ')
> 
> **参数:**
> **arr:**【array _ like】需要绝对值的数字数组。
> **out:**【n 数组，可选】存储结果的位置。如果提供，它必须具有输入广播到的形状。如果未提供或无，则返回新分配的数组。
> ****kwargs :** 允许将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> 
> **Return:**【n 数组或标量】arr 的绝对值，返回值总是浮点数。

**代码#1:工作**

```py
# Python program explaining
# fabs() function

import numpy as geek
in_num = 10
print ("Input  number : ", in_num)

out_num = geek.fabs(in_num) 
print ("Absolute value  of positive  input number : ", out_num) 
```

**输出:**

```py
Input  number :  10
Absolute value  of positive  input number :  10.0

```

**代码#2 :**

```py
# Python program explaining
# fabs() function

import numpy as geek
in_num = -9.0
print ("Input  number : ", in_num)

out_num = geek.fabs(in_num) 
print ("Absolute value  of negative input number : ", out_num) 
```

**输出:**

```py
Input  number :  -9.0
Absolute value  of negative input number :  9.0

```

**代码#3 :**

```py
# Python program explaining
# fabs() function

import numpy as geek

in_arr = [2, 0, -2, -5]
print ("Input array : ", in_arr)

out_arr = geek.fabs(in_arr) 
print ("Output absolute array : ", out_arr) 
```

**输出:**

```py
Input array :  [2, 0, -2, -5]
Output absolute array :  [ 2\.  0\.  2\.  5.]

```