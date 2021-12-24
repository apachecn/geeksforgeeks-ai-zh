# numpy 字符串操作| isnumeric()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-is numeric-function/](https://www.geeksforgeeks.org/numpy-string-operations-isnumeric-function/)

`numpy.core.defchararray.isnumeric(arr)`如果只有数字字符并且至少有一个字符，则函数为每个元素返回 true。否则返回 false。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。
> 
> **返回:**【ndarray】布尔的输出数组。

**代码#1 :**

```
# Python program explaining
# numpy.char.isnumeric() method 

import numpy as geek

# input array contains only numeric character
in_arr = geek.array([ '1000', '2000'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.isnumeric(in_arr)
print ("Output array: ", out_arr)
```

**Output:**

```
Input array :  ['1000' '2000']
Output array:  [ True  True]

```

**代码#2 :**

```
# Python program explaining
# numpy.char.isnumeric() method 

import numpy as geek

# input array 
in_arr = geek.array([ 'python3.5', 'a1000', '1234 ab'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.isnumeric(in_arr)
print ("Output array: ", out_arr)
```

**Output:**

```
Input array :  ['python3.5' 'a1000' '1234 ab']
Output array:  [False False False]

```