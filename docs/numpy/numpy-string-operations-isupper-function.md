# numpy 字符串操作| isupper()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-is upper-function/](https://www.geeksforgeeks.org/numpy-string-operations-isupper-function/)

**`numpy.core.defchararray.isupper(arr)`** 函数为每个元素返回 *True* 如果字符串中所有大小写字符都是大写的并且至少有一个字符，则返回 false。

> **参数:**
> **arr :** 字符串或 unicode 数组
> 
> **返回:**【ndarray】布尔的输出数组。

**代码#1:**

```
# Python Program explaining
# numpy.char.isupper() function 

import numpy as geek 

in_arr = geek.array(['P4Q R', '4Q rP', 'Q rp4', 'rpq'])
print ("input array : ", in_arr)

out_arr = geek.char.isupper(in_arr)
print ("output  array :", out_arr)
```

**Output:**

```
input array :  ['P4Q R' '4Q rP' 'Q rp4' 'rpq']
output array : [ True False False False]

```

**代码#2:**

```
# Python Program explaining
# numpy.char.isupper() function 

import numpy as geek 

in_arr = geek.array(['GEEKS', 'for', 'Geeks'])

print ("input array : ", in_arr)

out_arr = geek.char.isupper(in_arr)
print ("output array :", out_arr )
```

**Output:**

```
input array :  ['GEEKS' 'for' 'Geeks']
output array : [ True False False]

```