# numpy.asfortranarray()在 Python

中

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-asfortranarray-in-python/

**`numpy.asfortranarray()`** 函数用于当我们想要将输入转换为一个数组时，该数组在内存中以 Fortran 顺序排列。输入包括标量、列表、元组列表、元组、元组元组元组、列表元组和数组。

> **语法:** numpy.asfortranarray(arr，dtype=none)
> 
> **参数:**
> **arr:**【array _ like】输入数据，以任何可以转换为浮点型数组的形式。这包括标量、列表、元组列表、元组、元组元组元组、列表元组和数组。
> **数据类型:**默认情况下，数据类型是从输入数据中推断出来的。
> 
> **返回:**Fortran 中的输入 arr，或列主命令。

**代码#1:列表到数组**

```py
# Python program explaining
# numpy.asfortranarray() function

import numpy as geek
my_list = [1, 3, 5, 7, 9]

print ("Input  list : ", my_list)

out_arr = geek.asfortranarray(my_list)
print ("output fortanarray from input list : ", out_arr) 
```

**输出:**

```py
Input  list :  [1, 3, 5, 7, 9]
output fortanarray from input list :  [1 3 5 7 9]

```

**代码#2:福塔纳雷的元组**

```py
# Python program explaining
# numpy.asfortranarray() function

import numpy as geek

my_tuple = ([1, 3, 9], [8, 2, 6])

print ("Input  tuple : ", my_tuple)

out_arr = geek.asfortranarray(my_tuple, dtype ='int8') 
print ("output fortan array from input tuple : ", out_arr) 
```

**输出:**

```py
Input  tuple :  ([1, 3, 9], [8, 2, 6])
output fortan array from input touple :  [[1 3 9]
 [8 2 6]]

```

**代码#3:福塔纳雷的标量**

```py
# Python program explaining
# numpy.asfortranarray() function

import numpy as geek

my_scalar = 15

print ("Input  scalar : ", my_scalar)

out_arr = geek.asfortranarray(my_scalar, dtype ='float') 
print ("output fortan array from input scalar : ", out_arr) 
```

**输出:**

```py
Input  scalar :  15
output fortan array from input scalar :  [ 15.]

```

**代码#4:阵列到福塔纳雷**

```py
# Python program explaining
# numpy.asfortranarray() function

import numpy as geek

in_arr = geek.arange(9).reshape(3, 3)

print ("Input  array : ", in_arr)

# checking if it is fortanarray
print(in_arr.flags['F_CONTIGUOUS'])

out_arr = geek.asfortranarray(in_arr, dtype ='float') 
print ("output array from input array : ", out_arr) 

# checking if it has become fortanarray
print(out_arr.flags['F_CONTIGUOUS'])
```

**输出:**

```py
Input  array :  [[0 1 2]
 [3 4 5]
 [6 7 8]]
False
output array from input array :  [[ 0\.  1\.  2.]
 [ 3\.  4\.  5.]
 [ 6\.  7\.  8.]]
True

```