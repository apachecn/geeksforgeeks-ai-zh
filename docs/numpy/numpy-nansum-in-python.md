# python 中的 numpy . nansum()

> 原文:[https://www.geeksforgeeks.org/numpy-nansum-in-python/](https://www.geeksforgeeks.org/numpy-nansum-in-python/)

**`numpy.nansum()`** 函数用于计算给定轴上的数组元素之和，将非数字视为零。

> **语法:** numpy.nansum(arr，axis =无，dtype =无，out =无，keepdims= '无值')
> 
> **参数:**
> **arr:**【Array _ like】包含需要求和的数字的数组。如果 arr 不是数组，则尝试转换。
> **轴:**轴或计算总和的轴。默认值是计算展平数组的总和。
> **dtype :** 返回的数组的类型，以及对元素求和的累加器的类型。默认情况下，使用 arr 的*数据类型*。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **保持尺寸:**布尔，可选
> - >如果设置为真，减少的轴作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据原始 arr 正确广播。
> - >如果该值不是默认值，则 keepdims 将传递给 ndarray 子类的均值或求和方法。
> - >如果子类方法不实现 keepdims，将引发任何异常。
> 
> **Return :** 除非指定 out，否则将返回一个保存结果的新数组，在 out 中返回结果。结果的大小与 arr 相同，形状与 arr 相同，如果 axis 不是 None 或 arr，则为一维数组。

**代码#1:工作**

```py
# Python program explaining
# numpy.nansum() function

import numpy as geek
in_num = 10

print ("Input  number : ", in_num)

out_sum = geek.nansum(in_num) 
print ("sum of array element : ", out_sum) 
```

**输出:**

```py
Input  number :  10
sum of array element :  10

```

**代码#2 :**

```py
# Python program explaining
# numpy.nansum function

import numpy as geek

in_arr = geek.array([[2, 2, 2], [2, 2, geek.nan]])

print ("Input array : ", in_arr) 

out_sum = geek.nansum(in_arr) 
print ("sum of array elements: ", out_sum) 
```

**输出:**

```py
Input array :  [[  2\.   2\.   2.]
 [  2\.   2\.  nan]]
sum of array elements:  10.0

```

**代码#3 :**

```py
# Python program explaining
# numpy.nansum function

import numpy as geek

in_arr = geek.array([[2, 2, 2], [2, 2, geek.nan]])

print ("Input array : ", in_arr) 

out_sum = geek.nansum(in_arr, axis = 1) 
print ("sum of array elements taking axis 1: ", out_sum) 
```

**输出:**

```py
Input array :  [[  2\.   2\.   2.]
 [  2\.   2\.  nan]]
sum of array elements taking axis 1:  [ 6\.  4.]

```

**注意:**如果正无穷大和负无穷大都存在，总和将不是一个数(NaN)。如果正无穷大和负无穷大中的一个存在，总和将是正无穷大或负无穷大，这是存在的。

**代码#4 :**

```py
# Python program explaining
# numpy.nansum() function

import numpy as geek

in_arr1 = geek.array([2, -5, geek.nan, geek.inf])
in_arr2 = geek.array([1, 4, geek.inf, -geek.inf ])

print ("1st array elements: ", in_arr1) 
print ("2nd array elements: ", in_arr2) 

out_sum1 = geek.nansum(in_arr1) 
out_sum2 = geek.nansum(in_arr2)

print ("sum of 1st array elements: ", out_sum1) 
print ("sum of 2nd array elements: ", out_sum2) 
```

**输出:**

```py
1st array elements:  [  2\.  -5\.  nan  inf]
2nd array elements:  [  1\.   4\.  inf -inf]
sum of 1st array elements:  inf
sum of 2nd array elements:  nan

```