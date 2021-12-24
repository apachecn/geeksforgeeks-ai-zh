# numpy 字符串操作| islower()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-is lower-function/](https://www.geeksforgeeks.org/numpy-string-operations-islower-function/)

**`numpy.core.defchararray.islower(arr)`** 函数为每个元素返回 *True* 如果字符串中所有大小写字符都是小写，并且至少有一个大小写字符，则返回 false。

> **参数:**
> **arr :** 字符串或 unicode 数组
> 
> **返回:**【ndarray】布尔的输出数组。

**代码#1:**

```
# Python Program explaining
# numpy.char.islower() function 

import numpy as geek 

in_arr = geek.array(['P4Q R', '4Q rP', 'Q rp4', 'rpq'])
print ("input array : ", in_arr)

out_arr = geek.char.islower(in_arr)
print ("output  array :", out_arr)
```

**Output:**

```
input array :  ['P4Q R' '4Q rP' 'Q rp4' 'rpq']
output array : [False False False  True]

```

**代码#2:**

```
# Python Program explaining
# numpy.char.lower() function 

import numpy as geek 

in_arr = geek.array(['GEEKS', 'for', 'Geeks'])

print ("input array : ", in_arr)

out_arr = geek.char.islower(in_arr)
print ("output array :", out_arr )
```

**Output:**

```
input array :  ['GEEKS' 'for' 'Geeks']
output array : [False  True False]

```