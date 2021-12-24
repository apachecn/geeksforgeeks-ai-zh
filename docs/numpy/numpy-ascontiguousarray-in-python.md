# Python 中的 numpy.ascontiguousarray()

> 原文:[https://www . geeksforgeeks . org/numpy-ascontiguousarray-in-python/](https://www.geeksforgeeks.org/numpy-ascontiguousarray-in-python/)

**`numpy.ascontiguousarray()`** 函数是当我们想在内存中返回一个连续的数组时使用的(C 顺序)。

> **语法:**num py . ascntiguusarray(arr，dtype=None)
> 
> **参数:**
> **arr:**【array _ like】输入数据，以任何可以转换为数组的形式。这包括标量、列表、元组列表、元组、元组元组元组、列表元组和数组。
> **数据类型:**【字符串或数据类型对象，可选】返回数组的数据类型。
> 
> **返回:**n 与 arr 具有相同形状和内容的连续数组，如果指定了类型，则返回数据类型。

**代码#1:列表到数组**

```
# Python program explaining
# numpy.ascontiguousarray() function

import numpy as geek
my_list = [100, 200, 300, 400, 500]

print ("Input  list : ", my_list)

out_arr = geek.ascontiguousarray(my_list, dtype = geek.float32)
print ("output array from input list : ", out_arr) 
```

**输出:**

```
Input  list :  [100, 200, 300, 400, 500]
output array from input list :  [ 100\.  200\.  300\.  400\.  500.]

```

**代码#2:元组到数组**

```
# Python program explaining
# numpy.ascontiguousarray() function

import numpy as geek

my_tuple = ([2, 6, 10], [8, 12, 16])

print ("Input  tuple : ", my_tuple)

out_arr = geek.ascontiguousarray(my_tuple, dtype = geek.int32) 
print ("output array from input tuple : ", out_arr) 
```

**输出:**

```
Input  tuple :  ([2, 6, 10], [8, 12, 16])
output array from input tuple :  [[ 2  6 10]
 [ 8 12 16]]

```

**代码#3:标量到数组**

```
# Python program explaining
# numpy.ascontiguousarray() function

import numpy as geek

my_scalar = 100

print ("Input  scalar : ", my_scalar)

out_arr = geek.ascontiguousarray(my_scalar, dtype = geek.float32) 
print ("output array from input scalar : ", out_arr) 
print(type(out_arr))
```

**输出:**

```
Input  scalar :  100
output array from input scalar :  [ 100.]
class 'numpy.ndarray'

```