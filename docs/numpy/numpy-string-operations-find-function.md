# numpy 字符串操作| find()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-find-function/](https://www.geeksforgeeks.org/numpy-string-operations-find-function/)

`numpy.core.defchararray.find(arr, sub, start=0, end=None)`是 numpy 中做字符串运算的另一个函数。它返回字符串中最低的索引，在该索引中，arr 中的每个元素在从开始到结束的范围内都可以找到 substring sub。否则返回-1。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。
> **sub :** 【字符串或 unicode】要搜索的子字符串。
> **开始:**【int，可选】每个字符串中的开始位置。
> **结束:**【int，可选】每个字符串中的结束位置。
> 
> **返回:**【n 数组】输出整数数组。

**代码#1 :**

```
# Python program explaining
# numpy.char.find() method 

# importing numpy as geek
import numpy as geek

# input arrays  
in_arr = geek.array(['aAaAaA', 'baA', 'abBABba'])
print ("Input array : ", in_arr) 

# output arrays 
out_arr = geek.char.find(in_arr, sub ='A')
print ("Output array: ", out_arr) 
```

**Output:**

```
Input array :  ['aAaAaA' 'baA' 'abBABba']
Output array:  [1 2 3]

```

**代码#2 :**

```
# Python program explaining
# numpy.char.find() method 

# importing numpy as geek
import numpy as geek

# input arrays  
in_arr = geek.array(['aAaAaA', 'aA', 'abBABba'])
print ("Input array : ", in_arr) 

# output arrays 
out_arr = geek.char.find(in_arr, sub ='a', start = 3, end = 7)
print ("Output array: ", out_arr) 
```

**Output:**

```
Input array :  ['aAaAaA' 'aA' 'abBABba']
Output array:  [ 4 -1  6]

```