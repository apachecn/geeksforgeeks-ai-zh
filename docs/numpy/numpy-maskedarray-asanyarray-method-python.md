# Numpy MaskedArray asanyaray()方法| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-asanyaray-method-python/](https://www.geeksforgeeks.org/numpy-maskedarray-asanyarray-method-python/)

**`numpy.ma.asanyarray()`** 功能是在我们想要把输入转换成一个屏蔽数组时使用的，保存子类。
如果 arr 是 MaskedArray 的一个子类，那么它的类是保守的。如果输入已经是数组，则不执行复制。

> **语法:**num py . ma . asayar ray(arr，dtype=none)
> 
> **参数:**
> **arr:**【array _ like】输入数据，以任何可以转换为屏蔽数组的形式。
> **数据类型:**【数据类型，可选】默认情况下，数据类型是从输入数据中推断出来的。
> **顺序:**是使用行主(C 风格)还是列主(Fortran 风格)内存表示。默认为“C”。
> 
> **返回:**【屏蔽数组】arr 的屏蔽数组解释。

**代码#1 :**

```
# Python program explaining
# numpy.ma.asanyarray() function
import numpy as geek
my_list = [1, 4, 8, 7, 2, 5]

print ("Input list : ", my_list)

out_arr = geek.ma.asanyarray(my_list)
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
# numpy.ma.asanyarray() function

import numpy as geek

my_tuple = ([1, 4, 8], [7, 2, 5])

print ("Input tuple : ", my_tuple)

out_arr = geek.ma.asanyarray(my_tuple) 
print ("output array from input tuple : ", out_arr) 
```

**输出:**

```
Input tuple :  ([1, 4, 8], [7, 2, 5])
output array from input tuple :  [[1 4 8]
 [7 2 5]]

```