# numpy 字符串操作| strip()功能

> 原文:[https://www . geesforgeks . org/numpy-string-operations-strip-function/](https://www.geeksforgeeks.org/numpy-string-operations-strip-function/)

`numpy.core.defchararray.strip(arr, chars=None)`是 numpy 中做字符串运算的另一个函数。它为 arr 中的每个元素返回一个删除了前导和尾随字符的副本。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。
> **字符:**【字符串或 unicode，可选】要删除的字符集。如果省略或无，它将删除空白。chars 参数不是前缀或后缀；我们想要剥离的是它的所有价值组合。
> 
> **根据输入类型，返回字符串或 unicode 的输出数组。**

**代码#1 :**

```py
# Python program explaining
# numpy.char.strip() method 

import numpy as geek

# input arrays  
in_arr = geek.array(['Sun', '  Moon  ', 'Star'])
print ("Input array : ", in_arr) 

out_arr = geek.char.strip(in_arr)

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
# numpy.char.strip() method 

import numpy as geek

# input arrays  
in_arr = geek.array(['Sun', '  Moon  ', 'Star'])
print ("Input array : ", in_arr) 

out_arr = geek.char.strip(in_arr, chars ='Sun')

# 'Sun' removed from arr[0] as we have set chars = Sun
print ("Output array: ", out_arr) 
```

**Output:**

```py
Input array :  ['Sun' ' Moon ' 'Star']
Output array:  ['' ' Moon ' 'tar']

```

**代码#3 :**

```py
# Python program explaining
# numpy.char.strip() method 

import numpy as geek

# input arrays 
in_arr = geek.array([ 'Geeks', 'For', 'Geeks'] )
print ("Input array : ", in_arr) 

out_arr = geek.char.strip(in_arr, chars ='G')

#'G' removed from arr[0] and arr[2]
# as we have set chars ='G'
print ("Output array: ", out_arr) 
```

**Output:**

```py
Input array :  ['Geeks' 'For' 'Geeks']
Output array:  ['eeks' 'For' 'eeks']

```