# Python 中的 numpy.invert()

> 原文:[https://www.geeksforgeeks.org/numpy-invert-in-python/](https://www.geeksforgeeks.org/numpy-invert-in-python/)

**numpy.invert()** 函数用于逐位计算数组元素的**反演**。它计算输入数组中整数的基础二进制表示的位非。

对于有符号整数输入，返回两者的补码。在二进制补码系统中，负数由绝对值的二进制补码表示。

> **语法:** numpy.invert(x，/，out=None，*，其中=True，强制转换='same_kind '，顺序='K '，dtype=None，ufunc 'invert ')
> 
> **参数:**
> **x :** 【阵 _ 象】输入阵。
> **out:**【n 数组，可选】存储结果的位置。如果提供，它必须具有输入广播到的形状。如果未提供或无，则返回新分配的数组。
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> 
> **返回:**【数组或标量】结果。如果 x 是标量，这就是标量。

**代码#1:工作**

```py
# Python program explaining
# invert() function

import numpy as geek
in_num = 10
print ("Input  number : ", in_num)

out_num = geek.invert(in_num) 
print ("inversion of 10 : ", out_num) 
```

**输出:**

```py
Input  number :  10
inversion of 10 :  -11

```

**代码#2 :**

```py
# Python program explaining
# invert() function

import numpy as geek

in_arr = [2, 0, 25]
print ("Input array : ", in_arr)

out_arr = geek.invert(in_arr) 
print ("Output array after inversion: ", out_arr) 
```

**输出:**

```py
Input array :  [2, 0, 25]
Output array after inversion:  [ -3  -1 -26]

```

**代码#3 :**

```py
# Python program explaining
# invert() function

import numpy as geek

in_arr = [True, False]
print("Input array : ", in_arr) 

out_arr = geek.invert(in_arr) 
print ("Output array after inversion: ", out_arr) 
```

**输出:**

```py
Input array :  [True, False]
Output array after inversion:  [False  True]

```