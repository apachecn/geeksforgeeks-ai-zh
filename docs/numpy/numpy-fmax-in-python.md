# python 中的 numpy . fmax()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-fmx-in-python/

**`numpy.fmax()`** 函数用于计算数组元素的逐元素最大值。该函数比较两个数组，并返回一个包含元素方向最大值的新数组。

如果被比较的元素之一是 NaN，则返回非 nan 元素。如果两个元素都是 NAs，那么返回第一个。

> **语法:** numpy.fmax(arr1，arr2，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，ufunc 'fmax ')
> 
> **参数:**
> **arr 1:**【array _ like】保存待比较元素的数组。
> **arr 2:**【array _ like】保存待比较元素的数组。
> **out:**【n 数组，可选】存储结果的位置。如果提供，它必须具有输入广播到的形状。如果未提供或无，则返回新分配的数组。
> ****kwargs :** 允许将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> 
> **返回:**【数组或标量】arr1 和 arr2 的最大值，按元素计算。如果 arr1 和 arr2 都是标量，则返回标量。

**代码#1:工作**

```py
# Python program explaining
# fmax() function

import numpy as geek
in_num1 = 10
in_num2 = 11

print ("Input  number1 : ", in_num1)
print ("Input  number2 : ", in_num2) 

out_num = geek.fmax(in_num1, in_num2) 
print ("maximum of 10 and 11 : ", out_num) 
```

**输出:**

```py
Input  number1 :  10
Input  number2 :  11
maximum of 10 and 11 :  11

```

**代码#2 :**

```py
# Python program explaining
# fmax() function

import numpy as geek

in_arr1 = [2, 8, 125, geek.nan]
in_arr2 = [geek.nan, 3, 115, geek.nan]

print ("Input array1 : ", in_arr1) 
print ("Input array2 : ", in_arr2)

out_arr = geek.fmax(in_arr1, in_arr2) 
print ("Output array : ", out_arr) 
```

**输出:**

```py
Input array1 :  [2, 8, 125, nan]
Input array2 :  [nan, 3, 115, nan]
Output array :  [   2\.    8\.  125\.   nan]

```

**代码#3 :**

```py
# Python program explaining
# fmax() function

import numpy as geek

in_arr1 = [2, 8, 125]
in_arr2 = [3, 3, 115]

print ("Input array1 : ", in_arr1) 
print ("Input array2 : ", in_arr2)

out_arr = geek.fmax(in_arr1, in_arr2) 
print ("Output array: ", out_arr) 
```

**输出:**

```py
Input array1 :  [2, 8, 125]
Input array2 :  [3, 3, 115]
Output array:  [  3   8 125]

```