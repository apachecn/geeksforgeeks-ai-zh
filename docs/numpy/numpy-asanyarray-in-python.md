# python 中的 numpy . asanyarray()

> 原文:[https://www.geeksforgeeks.org/numpy-asanyarray-in-python/](https://www.geeksforgeeks.org/numpy-asanyarray-in-python/)

**`numpy.asanyarray()`** 函数用于当我们想要将输入转换为数组时，但是它通过了 *ndarray* 子类。输入可以是标量、列表、元组列表、元组、元组元组元组、列表元组和数组。

> **语法:**num py . asayar ray(arr，dtype=none，order=None)
> 
> **参数:**
> **arr:**【array _ like】输入数据，以任何可以转换为数组的形式。这包括标量、列表、元组列表、元组、元组元组元组、列表元组和数组。
> **数据类型:**【数据类型，可选】默认情况下，数据类型是从输入数据中推断出来的。
> **顺序:**是使用行主(C 风格)还是列主(Fortran 风格)内存表示。默认为“C”。
> 
> **返回:**【数组或数组子类】arr 的数组解释。如果 arr 是*数组*或数组的子类，则按原样返回，不执行复制。

**代码#1:列表到数组**

```py
# Python program explaining
# numpy.asanyarray() function

import numpy as geek
my_list = [1, 3, 5, 7, 9]

print ("Input  list : ", my_list)

out_arr = geek.asanyarray(my_list)
print ("output array from input list : ", out_arr) 
```

**输出:**

```py
Input  list :  [1, 3, 5, 7, 9]
output array from input list :  [1 3 5 7 9]

```

**代码#2:元组到数组**

```py
# Python program explaining
# numpy.asanyarray() function

import numpy as geek

my_tuple = ([1, 3, 9], [8, 2, 6])

print ("Input  tuple : ", my_tuple)

out_arr = geek.asanyarray(my_tuple) 
print ("output array from input tuple : ", out_arr) 
```

**输出:**

```py
Input  tuple :  ([1, 3, 9], [8, 2, 6])
output array from input tuple :  [[1 3 9]
 [8 2 6]]

```

**代码#3:标量到数组**

```py
# Python program explaining
# numpy.asanyarray() function

import numpy as geek

my_scalar = 12

print ("Input  scalar : ", my_scalar)

out_arr = geek.asanyarray(my_scalar) 
print ("output array from input scalar : ", out_arr) 
print(type(out_arr))
```

**输出:**

```py
Input  scalar :  12
output array from input scalar :  12
class 'numpy.ndarray'

```