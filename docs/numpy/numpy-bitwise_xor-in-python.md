# Python 中的 numpy.bitwise_xor()

> 原文:[https://www.geeksforgeeks.org/numpy-bitwise_xor-in-python/](https://www.geeksforgeeks.org/numpy-bitwise_xor-in-python/)

**numpy.bitwise_xor()** 函数用于计算两个数组元素的逐位**异或**。该函数计算输入数组中整数的基础二进制表示的逐位异或。

> **语法:** numpy.bitwise_xor(arr1，arr2，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，ufunc 'bitwise_xor ')
> 
> **参数:**
> **arr 1:**【array _ like】输入数组。
> **arr 2:**【array _ like】输入数组。
> **out:**【n 数组，可选】存储结果的位置。如果提供，它必须具有输入广播到的形状。如果未提供或无，则返回新分配的数组。
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> 
> **返回:**【数组或标量】结果。如果 x1 和 x2 都是标量，这就是标量。

**代码#1:工作**

```py
# Python program explaining
# bitwise_xor() function

import numpy as geek
in_num1 = 10
in_num2 = 11

print ("Input  number1 : ", in_num1)
print ("Input  number2 : ", in_num2) 

out_num = geek.bitwise_xor(in_num1, in_num2) 
print ("bitwise_xor of 10 and 11 : ", out_num) 
```

**输出:**

```py
Input  number1 :  10
Input  number2 :  11
bitwise_xor of 10 and 11 :  1

```

**代码#2 :**

```py
# Python program explaining
# bitwise_xor() function

import numpy as geek

in_arr1 = [2, 8, 125]
in_arr2 = [3, 3, 115]

print ("Input array1 : ", in_arr1) 
print ("Input array2 : ", in_arr2)

out_arr = geek.bitwise_xor(in_arr1, in_arr2) 
print ("Output array after bitwise_xor: ", out_arr) 
```

**输出:**

```py
Input array1 :  [2, 8, 125]
Input array2 :  [3, 3, 115]
Output array after bitwise_xor:  [ 1 11 14]

```

**代码#3 :**

```py
# Python program explaining
# bitwise_xor() function

import numpy as geek

in_arr1 = [True, False, True, False]
in_arr2 = [False, False, True, True]

print ("Input array1 : ", in_arr1) 
print ("Input array2 : ", in_arr2)

out_arr = geek.bitwise_xor(in_arr1, in_arr2) 
print ("Output array after bitwise_xor: ", out_arr) 
```

**输出:**

```py
Input array1 :  [True, False, True, False]
Input array2 :  [False, False, True, True]
Output array after bitwise_xor:  [ True False False  True]

```