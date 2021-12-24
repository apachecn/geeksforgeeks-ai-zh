# numpy 字符串运算| index()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-index-function/](https://www.geeksforgeeks.org/numpy-string-operations-index-function/)

`numpy.core.defchararray.index(arr, sub, start=0, end=None)`是 numpy 中做字符串运算的另一个函数。它返回字符串中最低的索引，在该索引中为 *arr* 中的每个元素找到子字符串 sub。如果 sub 不在 `[start, end]`范围内，则返回值错误。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。
> **sub :** 【字符串或 unicode】要搜索的子字符串。
> **开始:**【int，可选】每个字符串中的开始位置。
> **结束:**【int，可选】每个字符串中的结束位置。
> 
> **返回:**【n 数组】int 的输出数组。

**代码#1 :**

```
# Python program explaining
# numpy.char.index() method 

# importing numpy 
import numpy as geek

# input arrays  
in_arr = geek.array(['aAaAaA', 'baA', 'abBABba'])
print ("Input array : ", in_arr) 

# output arrays 
out_arr = geek.char.index(in_arr, sub ='a')
print ("Output array: ", out_arr) 
```

**Output:**

```
Input array :  ['aAaAaA' 'baA' 'abBABba']
Output array:  [0 1 0]

```

**代码#2 :**

```
# Python program explaining
# numpy.char.index() method 

# importing numpy 
import numpy as geek

# input arrays  
in_arr = geek.array(['aAaAaA', 'aA', 'abBABba'])
print ("Input array : ", in_arr) 

# output arrays 
out_arr = geek.char.index(in_arr, sub ='A', start = 1, end = 4)
print ("Output array: ", out_arr) 
```

**Output:**

```
Input array :  ['aAaAaA' 'aA' 'abBABba']
Output array:  [1 1 3]

```

**代码#3 :** 如果没有找到子字符串，则引发 ValueError。

```
# Python program explaining
# numpy.char.index() method 

# importing numpy 
import numpy as geek

# input arrays  
in_arr = geek.array(['aAaAaA', 'aA', 'abBABba'])
print ("Input array : ", in_arr) 

# output arrays 
out_arr = geek.char.index(in_arr, sub ='A', start = 3, end = 7)
print ("Output array: ", out_arr) 
```

**Output:**

```
ValueError: substring not found

```