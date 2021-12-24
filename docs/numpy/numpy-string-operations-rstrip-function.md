# numpy 字符串操作| rstrip()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-rst rip-function/](https://www.geeksforgeeks.org/numpy-string-operations-rstrip-function/)

`numpy.core.defchararray.rstrip(arr, chars=None)`是 numpy 中做字符串运算的另一个函数。它返回一个副本，其中删除了 *arr* 中每个元素的尾随字符。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。
> **字符:**【字符串或 unicode，可选】要删除的字符集。如果省略或无，它将删除空白。chars 参数不是前缀或后缀；我们想要剥离的是它的所有价值组合。
> 
> **根据输入类型，返回字符串或 unicode 的输出数组。**

**代码#1 :**

```py
# Python program explaining
# numpy.char.rstrip() method 

import numpy as geek

# input arrays  
in_arr = geek.array(['Sun', '  Moon  ', 'Star'])
print ("Input array : ", in_arr) 

out_arr = geek.char.rstrip(in_arr)

# whitespace removed from arr[1] 
# as we have set chars = None
print ("Output array: ", out_arr) 
```

**Output:**

```py
Input array :  ['Sun' ' Moon ' 'Star']
Output array:  ['Sun' 'Moon' 'Star']

```

**代码#2 :**

```py
# Python program explaining
# numpy.char.rstrip() method 

import numpy as geek

# input arrays 
in_arr = geek.array([ 'Geeks', 'For', 'Geeks'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.rstrip(in_arr, chars ='s')

#'s' removed from arr[0] and 
# arr[2] as we have set chars ='s'
print ("Output array: ", out_arr) 
```

**Output:**

```py
Input array :  ['Geeks' 'For' 'Geeks']
Output array:  ['Geek' 'For' 'Geek']

```

**代码#3 :**

```py
# Python program explaining
# numpy.char.rstrip() method 

import numpy as geek

# input arrays 
in_arr = geek.array([ 'GeeksG', 'ForG', 'Geeks'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.rstrip(in_arr, chars ='G')

# will strip 'G' from right side
# from each element(if exists)
print ("Output array: ", out_arr) 
```

**Output:**

```py
Input array :  ['GeeksG' 'ForG' 'Geeks']
Output array:  ['Geeks' 'For' 'Geeks']

```