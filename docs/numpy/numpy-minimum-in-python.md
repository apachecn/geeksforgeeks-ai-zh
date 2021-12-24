# Python 中的 numpy.minimum()

> 原文:[https://www.geeksforgeeks.org/numpy-minimum-in-python/](https://www.geeksforgeeks.org/numpy-minimum-in-python/)

**`numpy.minimum()`** 函数用于寻找数组元素的元素方向最小值。

它比较两个数组，并返回一个包含元素方向最小值的新数组。如果被比较的元素之一是 NaN，则返回该元素。如果两个元素都是 NAs，那么返回第一个。

> **语法:** numpy.minimum(arr1，arr2，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，ufunc 'minimum ')
> 
> **参数:**
> **arr 1:**【array _ like】输入数组。
> **arr 2:**【array _ like】输入数组。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> 
> **返回:**【数组或标量】结果。
> 元素方面，arr1 和 arr2 的最小值。如果 arr1 和 arr2 都是标量，这就是标量。

**代码#1:工作**

```
# Python program explaining
# minimum() function

import numpy as geek
in_num1 = 10
in_num2 = 21

print ("Input  number1 : ", in_num1)
print ("Input  number2 : ", in_num2) 

out_num = geek.minimum(in_num1, in_num2) 
print ("minimum of 10 and 21 : ", out_num) 
```

**输出:**

```
Input  number1 :  10
Input  number2 :  21
minimum of 10 and 21 :  10

```

**代码#2 :**

```
# Python program explaining
# minimum() function

import numpy as geek

in_arr1 = [2, 8, 125]
in_arr2 = [3, 3, 15]

print ("Input array1 : ", in_arr1) 
print ("Input array2 : ", in_arr2)

out_arr = geek.minimum(in_arr1, in_arr2) 
print ("Output array after selecting minimum: ", out_arr) 
```

**输出:**

```
Input array1 :  [2, 8, 125]
Input array2 :  [3, 3, 15]
Output array after selecting minimum:  [ 2  3 15]

```

**代码#3 :**

```
# Python program explaining
# minimum() function

import numpy as geek

in_arr1 = [geek.nan, 0, geek.nan]
in_arr2 = [geek.nan, geek.nan, 0]

print ("Input array1 : ", in_arr1) 
print ("Input array2 : ", in_arr2)

out_arr = geek.minimum(in_arr1, in_arr2) 
print ("Output array after selecting minimum: ", out_arr) 
```

**输出:**

```
Input array1 :  [nan, 0, nan]
Input array2 :  [nan, nan, 0]
Output array after selecting minimum:  [ nan  nan  nan]

```