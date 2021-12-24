# Numpy MaskedArray asarray()方法| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-asar ray-method-python/](https://www.geeksforgeeks.org/numpy-maskedarray-asarray-method-python/)

**`numpy.ma.asarray()`** 函数在我们想要将输入转换为给定数据类型的屏蔽数组时使用。
如果输入已经是数组，则不执行复制。如果 arr 是 maskearray 的子类，则返回一个基类 maskearray。

> **语法:** numpy.ma.asarray(arr，dtype=none，order=None)
> 
> **参数:**
> **arr:**【array _ like】输入数据，以任何可以转换为屏蔽数组的形式。这包括列表、元组列表、元组、元组元组元组、列表元组、数组和屏蔽数组。
> **数据类型:**【数据类型，可选】默认情况下，数据类型是从输入数据中推断出来的。
> **顺序:**是使用行主(C 风格)还是列主(Fortran 风格)内存表示。默认为“C”。
> 
> **返回:**【屏蔽数组】arr 的屏蔽数组解释。

**代码#1 :**

```
# Python program explaining
# numpy.ma.asarray() function
import numpy as geek
my_list = [1, 4, 8, 7, 2, 5]

print ("Input list : ", my_list)

out_arr = geek.ma.asarray(my_list)
print ("output array from input list : ", out_arr) 
```

**输出:**

```
Input list :  [1, 4, 8, 7, 2, 5]
output array from input list :  [1 4 8 7 2 5]

```

**代码#2 :**

```
# Python program explaining
# numpy.ma.asarray() function

import numpy as geek

my_tuple = ([1, 4, 8], [7, 2, 5])

print ("Input tuple : ", my_tuple)

out_arr = geek.ma.asarray(my_tuple) 
print ("output array from input tuple : ", out_arr) 
```

**输出:**

```
Input tuple :  ([1, 4, 8], [7, 2, 5])
output array from input tuple :  [[1 4 8]
 [7 2 5]]

```