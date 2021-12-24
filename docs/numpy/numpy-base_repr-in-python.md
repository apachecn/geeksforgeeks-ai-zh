# numpy.base_repr()用 Python

表示

> 原文:[https://www.geeksforgeeks.org/numpy-base_repr-in-python/](https://www.geeksforgeeks.org/numpy-base_repr-in-python/)

**`numpy.base_repr(number, base=2, padding=0)`** 函数用于返回给定基本系统中一个数字的字符串表示。

例如，十进制数字 10 在二进制中表示为 1010，而在八进制中表示为 12。

> **语法:** numpy.base_repr(number，base=2，padding=0)
> 
> **参数:**
> **编号:**输入编号。只有整数十进制数可以用作输入。
> **底数:**【int，可选】将数字转换为底数系统。有效范围为 2-36，默认值为 2。
> **填充:**【int，可选】在左边添加零的个数。默认值为 0。
> 
> **返回:**基本系统中输入数字的字符串表示。

**代码#1:工作**

```py
# Python program explaining
# base_repr() function

import numpy as geek
in_num = 10

print ("Input  number : ", in_num)

out_num = geek.base_repr(in_num, base = 2, padding = 0) 
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
# base_repr() function
import numpy as geek

in_arr = [5, -8, 21 ]

print ("Input array : ", in_arr) 
print()

# binary representation of first array  
# element without using padding parameter
out_num = geek.base_repr(in_arr[0], base = 2)
print("binary representation of 5")
print ("Without using padding parameter : ", out_num) 

# binary representation of first array
# element using padding parameter
out_num = geek.base_repr(in_arr[0], base = 2, padding = 3)
print ("Using padding parameter: ", out_num)
print()

# octal representation of 2nd array
# element without using width parameter
out_num = geek.base_repr(in_arr[1], base = 8, padding = 0)
print("octal representation of -8")
print ("Without using padding parameter : ", out_num) 

# octal representation of 2nd array
# element  using padding parameter
out_num = geek.base_repr(in_arr[1], base = 8, padding = 4)
print ("Using padding parameter : ", out_num) 
print()

# hexa-decimal representation of 3rd array
# element without using padding parameter
out_num = geek.base_repr(in_arr[2], base = 16, padding = 0)
print("hexa-decimal representation of 21")
print ("Without using padding parameter : ", out_num) 

# hexa-decimal representation of 3rd array
# element  using padding parameter
out_num = geek.base_repr(in_arr[2], base = 16, padding = 3)
print ("Using padding parameter : ", out_num) 
```

**输出:**

```py
Input array :  [5, -8, 21]

binary representation of 5
Without using padding parameter :  101
Using padding parameter:  000101

octal representation of -8
Without using padding parameter :  -10
Using padding parameter :  -000010

hexa-decimal representation of 21
Without using padding parameter :  15
Using padding parameter :  00015
```