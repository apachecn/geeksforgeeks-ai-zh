# python 中的 numpy.nanprod()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-nanprod-in-python/

**`numpy.nanprod()`** 函数用于计算给定轴上数组元素的乘积，将`NaNs` 视为 1。对于全为-NaN 或空的切片，返回一个。

> **语法:** numpy.nanprod(arr，axis=None，dtype=None，out=None，keepdims='class numpy。_ 全局。_NoValue ')。
> 
> **参数:**
> **arr:**【Array _ like】包含需要求和的数字的数组。如果 arr 不是数组，则尝试转换。
> **轴:**计算产品的轴。默认情况下，计算展平数组的乘积。
> **dtype :** 返回的数组的类型，以及对元素求和的累加器的类型。默认情况下，使用 arr 的*数据类型*。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **保持尺寸:**如果设置为真，减少的轴将作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据原始 arr 正确广播。
> 
> **Return :** 除非指定 out，否则将返回一个保存结果的新数组，在这种情况下，将返回该数组。

**代码#1:工作**

```py
# Python program explaining
# numpy.nanprod() function

import numpy as geek
in_num = 10

print ("Input  number : ", in_num)

out_prod = geek.nanprod(in_num) 
print ("product of array element : ", out_prod) 
```

**输出:**

```py
Input  number :  10
product of array element :  10

```

**代码#2 :**

```py
# Python program explaining
# numpy.nanprod function

import numpy as geek

in_arr = geek.array([[2, 2, 2], [2, 2, geek.nan]])

print ("Input array : ", in_arr) 

out_prod = geek.nanprod(in_arr) 
print ("product of array elements: ", out_prod) 
```

**输出:**

```py
Input array :  [[  2\.   2\.   2.]
 [  2\.   2\.  nan]]
product of array elements:  32.0

```

**代码#3 :**

```py
# Python program explaining
# numpy.nanprod function

import numpy as geek

in_arr = geek.array([[2, 2, 2], [2, 2, geek.nan]])

print ("Input array : ", in_arr) 

out_prod = geek.nanprod(in_arr, axis = 1) 
print ("product of array elements taking axis 1: ", out_prod) 
```

**输出:**

```py
Input array :  [[  2\.   2\.   2.]
 [  2\.   2\.  nan]]
product of array elements taking axis 1:  [ 8\.  4.]

```