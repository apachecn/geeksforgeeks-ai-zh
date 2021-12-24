# numpy 字符串操作| isalpha()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-isalpha-function/](https://www.geeksforgeeks.org/numpy-string-operations-isalpha-function/)

如果字符串中的所有字符都是字母并且至少有一个字符，则`numpy.core.defchararray.isalpha(arr)`函数为每个元素返回*True*；否则返回 false。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。
> 
> **返回:**【ndarray】布尔的输出数组。

**代码#1 :**

```
# Python program explaining
# numpy.char.isalpha() method 

import numpy as geek

# input array
in_arr = geek.array([ 'abcd', 'ac1bd', 'abdc', 'dcba', 'ab cd'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.isalpha(in_arr)
print ("Output array: ", out_arr)
```

**Output:**

```
Input array :  ['abcd' 'ac1bd' 'abdc' 'dcba' 'ab cd']
Output array:  [ True False  True  True False]

```

**代码#2 :**

```
# Python program explaining
# numpy.char.isalpha() method 

import numpy as geek

# input array
in_arr = geek.array([ 'geeks', 'for', 'geeks', 'wow !'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.isalpha(in_arr)
print ("Output array: ", out_arr)
```

**Output:**

```
Input array :  ['geeks' 'for' 'geeks' 'wow!']
Output array:  [ True  True  True False]

```