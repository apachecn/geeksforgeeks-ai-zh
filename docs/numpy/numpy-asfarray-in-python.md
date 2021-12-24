# Python 中的 numpy.asfarray()

> 原文:[https://www.geeksforgeeks.org/numpy-asfarray-in-python/](https://www.geeksforgeeks.org/numpy-asfarray-in-python/)

**`numpy.asfarray()`** 功能是在我们想要将输入转换为浮点型数组时使用的。输入包括标量、列表、元组列表、元组、元组元组元组、列表元组和数组。

> **语法:** numpy.asfarray(arr，dtype=type ' numpy . float 64 ')"
> 
> **参数:**
> **arr:**【array _ like】输入数据，以任何可以转换为浮点型数组的形式。这包括标量、列表、元组列表、元组、元组元组元组、列表元组和数组。
> **数据类型:**强制输入数组 arr 的浮点型代码。如果数据类型是“int”数据类型之一，它将被 float64 替换。
> 
> **返回:**【数组】输入数组为浮点数组。

**代码#1:列表到浮点型数组**

```
# Python program explaining
# numpy.asfarray() function

import numpy as geek
my_list = [1, 3, 5, 7, 9]

print ("Input  list : ", my_list)

out_arr = geek.asfarray(my_list)
print ("output float type array from input list : ", out_arr) 
```

**输出:**

```
Input  list :  [1, 3, 5, 7, 9]
output float type array from input list :  [ 1\.  3\.  5\.  7\.  9.]

```

**代码#2:元组到浮点型数组**

```
# Python program explaining
# numpy.asfarray() function

import numpy as geek

my_tuple = ([1, 3, 9], [8, 2, 6])

print ("Input  tuple : ", my_tuple)

out_arr = geek.asfarray(my_tuple, dtype ='int8') 
print ("output float type array from input tuple : ", out_arr) 
```

**输出:**

```
Input  tuple :  ([1, 3, 9], [8, 2, 6])
output float type array from input tuple :  [[ 1\.  3\.  9.]
 [ 8\.  2\.  6.]]

```

**代码#3:标量到浮点型数组**

```
# Python program explaining
# numpy.asfarray() function

import numpy as geek

my_scalar = 15

print ("Input  scalar : ", my_scalar)

out_arr = geek.asfarray(my_scalar, dtype ='float') 
print ("output float type array from input scalar : ", out_arr) 
```

**输出:**

```
InInput  scalar :  15
output float type array from input scalar :  15.0

```