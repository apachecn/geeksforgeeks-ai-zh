# Numpy str_len()功能

> 原文:[https://www.geeksforgeeks.org/numpy-str_len-function/](https://www.geeksforgeeks.org/numpy-str_len-function/)

`numpy.char.str_len(arr)`函数用于在 numpy 中进行字符串运算。它返回每个字符串元素的长度。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。输入数组。
> 
> **返回:**【n 数组】整数输出数组。

**代码#1 :**

```py
# Python program explaining
# numpy.char.str_len() method 

# importing numpy 
import numpy as geek

# input array  
in_arr = geek.array(['geeks for geeks'])
print ("Input array : ", in_arr) 

# output array 
out_arr = geek.char.str_len(in_arr)
print ("Output array containing length: ", out_arr) 
```

**Output:**

```py
Input array :  ['geeks for geeks']
Output array containing length:  [15]

```

**代码#2 :**

```py
# Python program explaining
# numpy.char.str_len() method 

# importing numpy 
import numpy as geek

# input array 
in_arr = geek.array(['Numpy', 'Python', 'Pandas'])
print ("Input array : ", in_arr) 

# output array 
out_arr = geek.char.str_len(in_arr)
print ("Output array containing length: ", out_arr) 
```

**Output:**

```py
Input array :  ['Numpy' 'Python' 'Pandas']
Output array containing length:  [5 6 6]

```