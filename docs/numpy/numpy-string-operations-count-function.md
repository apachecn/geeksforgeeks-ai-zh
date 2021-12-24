# numpy 字符串操作|计数()功能

> 原文:[https://www . geesforgeks . org/numpy-string-operations-count-function/](https://www.geeksforgeeks.org/numpy-string-operations-count-function/)

`numpy.core.defchararray.count(arr, sub, start=0, end=None)`是 numpy 中做字符串运算的另一个函数。它返回一个数组，子字符串 sub 在从开始到结束的范围内不重叠出现的次数。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。
> **sub :** 【字符串或 unicode】要搜索的子字符串。
> **开始:**【int，可选】每个字符串中的开始位置。
> **结束:**【int，可选】每个字符串中的结束位置。
> 
> **返回:**【n 数组】子串 sub 不重叠出现的次数。

**代码#1 :**

```
# Python program explaining
# numpy.char.count() method 

# importing numpy as geek
import numpy as geek

# input arrays  
in_arr = geek.array(['Sayantan', '  Sayan  ', 'Sayansubhra'])
print ("Input array : ", in_arr) 

# output arrays 
out_arr = geek.char.count(in_arr, sub ='an')
print ("Output array: ", out_arr) 
```

**Output:**

```
Input array :  ['Sayantan' ' Sayan ' 'Sayansubhra']
Output array:  [2 1 1]

```

**代码#2 :**

```
# Python program explaining
# numpy.char.count() method 

# importing numpy as geek
import numpy as geek

# input arrays  
in_arr = geek.array(['Sayantan', '  Sayan  ', 'Sayansubhra'])
print ("Input array : ", in_arr) 

# output arrays 
out_arr = geek.char.count(in_arr, sub ='a', start = 1, end = 8)
print ("Output array: ", out_arr) 
```

**Output:**

```
Input array :  ['Sayantan' ' Sayan ' 'Sayansubhra']
Output array:  [3 2 2]

```