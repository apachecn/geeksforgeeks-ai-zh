# numpy.asarray()在 Python

中

> 原文:[https://www.geeksforgeeks.org/numpy-asarray-in-python/](https://www.geeksforgeeks.org/numpy-asarray-in-python/)

**`numpy.asarray()`** 功能是在我们想要将输入转换成数组时使用的。输入可以是列表、元组列表、元组、元组元组元组、列表元组和数组。

> **语法:** numpy.asarray(arr，dtype =无，order =无)
> 
> **参数:**
> **arr:**【array _ like】输入数据，以任何可以转换为数组的形式。这包括列表、元组列表、元组、元组元组元组、列表元组和数组。
> **数据类型:**【数据类型，可选】默认情况下，数据类型是从输入数据中推断出来的。
> **顺序:**是使用行主(C 风格)还是列主(Fortran 风格)内存表示。默认为“C”。
> 
> **返回:**【ndarray】arr 的数组解释。如果输入已经是具有匹配数据类型和顺序的*数组*，则不执行复制。如果 arr 是 ndarray 的子类，则返回基类 ndarray。

**代码#1:列表到数组**

```
# Python program explaining
# numpy.asarray() function

import numpy as geek
my_list = [1, 3, 5, 7, 9]

print ("Input  list : ", my_list)

out_arr = geek.asarray(my_list)
print ("output array from input list : ", out_arr) 
```

**输出:**

```
Input  list :  [1, 3, 5, 7, 9]
output array from input list :  [1 3 5 7 9]

```

**代码#2:元组到数组**

```
# Python program explaining
# numpy.asarray() function

import numpy as geek

my_tuple = ([1, 3, 9], [8, 2, 6])

print ("Input  tuple : ", my_tuple)

out_arr = geek.asarray(my_tuple) 
print ("output array from input tuple : ", out_arr) 
```

**输出:**

```
Input  tuple :  ([1, 3, 9], [8, 2, 6])
output array from input tuple :  [[1 3 9]
 [8 2 6]]

```