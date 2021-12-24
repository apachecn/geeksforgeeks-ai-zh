# Python 中的 numpy.binary_repr()

> 原文:[https://www.geeksforgeeks.org/numpy-binary_repr-in-python/](https://www.geeksforgeeks.org/numpy-binary_repr-in-python/)

**`numpy.binary_repr(number, width=None)`** 函数用于将输入数字的二进制形式表示为字符串。

对于负数，如果没有给定宽度，则在前面加一个减号。如果给定宽度，则返回该数字相对于该宽度的二进制补码。
在二进制补码系统中，负数用绝对值的二进制补码表示。这是计算机上表示有符号整数的最常见方法。

> **语法:** numpy.binary_repr(数字，宽度=无)
> 
> **参数:**
> **编号:**输入编号。只有整数十进制数可以用作输入。
> **宽度:**【int，可选】如果 number 为正数，则返回字符串的长度，如果 number 为负数，则返回二进制补码的长度，前提是宽度至少要有足够的位数，以便 number 以指定的形式表示。
> 如果宽度值不足，将被忽略，数字将以二进制(数字> 0)或二进制补码(数字< 0)形式返回，其宽度等于以指定形式表示数字所需的最小位数。
> 
> **返回:**输入数字的二进制字符串表示。

**代码#1:工作**

```py
# Python program explaining
# binary_repr() function

import numpy as geek
in_num = 10

print ("Input  number : ", in_num)

out_num = geek.binary_repr(in_num) 
print ("binary representation of 10 : ", out_num) 
```

**输出:**

```py
Input  number :  10
binary representation of 10 :  1010

```

**代码#2 :**

```py
# Python program explaining
# binary_repr() function
import numpy as geek

in_arr = [5, -8 ]

print ("Input array : ", in_arr) 

# binary representation of first array  
# element without using width parameter
out_num = geek.binary_repr(in_arr[0])
print("Binary representation of 5")
print ("Without using width parameter : ", out_num) 

# binary representation of first array
# element using width parameter
out_num = geek.binary_repr(in_arr[0], width = 5)
print ("Using width parameter: ", out_num) 

print("\nBinary representation of -8")

# binary representation of 2nd array
# element without using width parameter
out_num = geek.binary_repr(in_arr[1])
print ("Without using width parameter : ", out_num) 

# binary representation of 2nd array
# element  using width parameter
out_num = geek.binary_repr(in_arr[1], width = 5)
print ("Using width parameter : ", out_num) 
```

**输出:**

```py
Input array :  [5, -8]
Binary representation of 5 
Without using width parameter :  101
Using width parameter:  00101

Binary representation of -8  
Without using width parameter :  -1000
Using width parameter :  11000
```