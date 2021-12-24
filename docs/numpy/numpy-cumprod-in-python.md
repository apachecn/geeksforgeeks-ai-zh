# python 中的 num py . cumber()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-cumber-in-python/

**`numpy.cumprod()`** 函数用于计算给定轴上数组元素的累积积。

> **语法:** numpy.cumprod(arr，axis =无，dtype =无，out =无)
> 
> **参数:**
> **arr:**【Array _ like】包含需要其累积积的数字的数组。如果 arr 不是数组，则尝试转换。
> **轴:**计算累积积的轴。默认情况下，计算展平数组的乘积。
> **数据类型:**返回数组的类型，以及元素相乘的累加器的类型。如果未指定 dtype，则默认为 arr 的 dtype，除非 arr 具有精度小于默认平台整数的整数 dtype。在这种情况下，将使用默认的平台整数。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **Return :** 除非指定 out，否则将返回一个保存结果的新数组，在这种情况下，将返回该数组。

**代码#1:工作**

```
# Python program explaining
# numpy.cumprod() function

import numpy as geek

in_num = 10

print ("Input  number : ", in_num)

out_prod = geek.cumprod(in_num) 
print ("cumulative product of input number : ", out_prod) 
```

**输出:**

```
Input  number :  10
cumulative product of input number :  [10]

```

**代码#2 :**

```
# Python program explaining
# numpy.cumprod() function

import numpy as geek

in_arr = geek.array([[2, 4, 6], [1, 3, 5]])

print ("Input array : ", in_arr) 

out_prod = geek.cumprod(in_arr) 
print ("cumulative product of array elements: ", out_prod) 
```

**输出:**

```
Input array :  [[2 4 6]
 [1 3 5]]
cumulative product of array elements:  [  2   8  48  48 144 720]

```

**代码#3 :**

```
# Python program explaining
# numpy.cumprod() function

import numpy as geek

in_arr = geek.array([[2, 4, 6], [1, 3, 5]])

print ("Input array : ", in_arr) 

out_prod = geek.cumprod(in_arr, axis = 1) 
print ("cumulative product of array elements taking axis 1: ", out_prod) 
```

**输出:**

```
Input array :  [[2 4 6]
 [1 3 5]]
cumulative product of array elements taking axis 1:  [[ 2  8 48]
 [ 1  3 15]]

```