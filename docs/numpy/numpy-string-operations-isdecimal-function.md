# numpy 字符串操作| isdecimal()函数

> 原文:[https://www . geeksforgeeks . org/numpy-string-operations-is decimal-function/](https://www.geeksforgeeks.org/numpy-string-operations-isdecimal-function/)

如果元素中只有十进制字符，则`numpy.core.defchararray.isdecimal(arr)`函数为每个元素返回*真*。否则返回 false。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。
> 
> **返回:**【ndarray】布尔的输出数组。

**代码#1 :**

```py
# Python program explaining
# numpy.char.isdecimal() method 

import numpy as geek

# input array contains only digits
in_arr = geek.array([ '1000', '2000'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.isdecimal(in_arr)
print ("Output array: ", out_arr)
```

**Output:**

```py
Input array :  ['1000' '2000']
Output array:  [ True  True]

```

**代码#2 :**

```py
# Python program explaining
# numpy.char.isdecimal() method 

import numpy as geek

# input array contains digits along with space and alphabets
in_arr = geek.array([ '1000 2', 'a1000', '1234 ab'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.isdecimal(in_arr)
print ("Output array: ", out_arr)
```

**Output:**

```py
Input array :  ['1000 2' 'a1000' '1234 ab']
Output array:  [False False False]

```