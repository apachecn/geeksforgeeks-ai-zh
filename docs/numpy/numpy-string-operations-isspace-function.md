# numpy 字符串操作| isspace()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-is space-function/](https://www.geeksforgeeks.org/numpy-string-operations-isspace-function/)

`numpy.core.defchararray.isspace(arr)`如果字符串中只有空白字符并且至少有一个字符，则函数为每个元素返回 true。否则返回 false。

> **语法:** numpy.core.isspace(arr)
> 
> **参数:**
> **arr :** 类似字符串或 unicode 的数组。
> 
> **返回:**【ndarray】布尔的输出数组。

**代码#1 :**

```
# Python program explaining
# numpy.char.isspace() method 

import numpy as geek

# input arrays  not containing any space
in_arr = geek.array([ 'Geeksforgeeks', 'Codechef'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.isspace(in_arr)
print ("Output array: ", out_arr)
```

**Output:**

```
Input array :  ['Geeksforgeeks' 'Codechef']
Output array:  [False False]

```

**代码#2 :**

```
# Python program explaining
# numpy.char.isspace() method 

import numpy as geek

# input arrays containing string along with space
in_arr = geek.array([ 'Geeks\nfor\ngeeks', 'Code\tchef'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.isspace(in_arr)
print ("Output array: ", out_arr)
```

**Output:**

```
Input array :  ['Geeks\nfor\ngeeks' 'Code\tchef']
Output array:  [False False]

```

**代码#3 :**

```
# Python program explaining
# numpy.char.isspace() method 

import numpy as geek

# input arrays containing only white space
in_arr = geek.array([ '\n', '\t', ' ', '\n\t '] )
print ("Input array : ", in_arr) 

out_arr = geek.char.isspace(in_arr)
print ("Output array: ", out_arr)
```

**Output:**

```
Input array :  ['\n' '\t' ' ' '\n\t ']
Output array:  [ True  True  True  True]

```