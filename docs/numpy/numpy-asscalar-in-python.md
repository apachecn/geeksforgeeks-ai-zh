# python 中的 numpy . asscalar()

> 原文:[https://www.geeksforgeeks.org/numpy-asscalar-in-python/](https://www.geeksforgeeks.org/numpy-asscalar-in-python/)

**`numpy.asscalar()`** 函数用于当我们想要将一个大小为 1 的数组转换为它的标量等价物时。

> **语法:**num py . asslar(arr)
> 
> **参数:**
> **arr:**【ndarray】输入大小为 1 的数组。
> 
> **返回:**arr 的标量表示。输出数据类型与输入的 item 方法返回的类型相同。

**代码#1:工作**

```py
# Python program explaining
# numpy.asscalar() function

import numpy as geek
# creating a array of size 1
in_arr = geek.array([ 8 ])

print ("Input  array : ", in_arr)

out_scalar = geek.asscalar(in_arr)
print ("output scalar from input array : ", out_scalar) 
```

**输出:**

```py
Input  array :  [8]
output scalar from input array :  8

```

**代码#2 :**

```py
# Python program explaining
# numpy.asscalar() function
import numpy as geek

in_list = [2 ]

# changing the list to size 1 array
arr = geek.array(in_list) 

print ("Input  array from list : ", arr)

# changing the array to scalar  
scalar = geek.asscalar(arr)

print ("output scalar from input list : ", scalar) 
```

**输出:**

```py
Input  array from list :  [2]
output scalar from input list :  2

```