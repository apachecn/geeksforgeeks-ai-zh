# numpy 字符串操作| istitle()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-istitle-function/](https://www.geeksforgeeks.org/numpy-string-operations-istitle-function/)

**`numpy.core.defchararray.istitle(arr)`** 函数为数组中的每个元素返回 *True* 如果元素是一个带标题的字符串并且至少有一个字符，则返回 false。

> **参数:**
> **arr :** 字符串或 unicode 数组
> 
> **返回:**【ndarray】布尔的输出数组。

**代码#1:**

```
# Python Program explaining
# numpy.char.istitle() function 

import numpy as geek 

in_arr = geek.array(['P4Q R', '4Q Rp', 'Q rP4', 'Rpq'])
print ("input array : ", in_arr)

out_arr = geek.char.istitle(in_arr)
print ("output  array :", out_arr)
```

**Output:**

```
input array :  ['P4Q R' '4Q Rp' 'Q rP4' 'Rpq']
output array : [ True  True False  True]

```

  **Code #2:**

```
# Python Program explaining 
# numpy.char.istitle() function  

import numpy as geek  

in_arr = geek.array(['GEEKS', 'for', 'Geeks']) 

print ("input array : ", in_arr) 

out_arr = geek.char.istitle(in_arr) 
print ("output array :", out_arr ) 
```

**Output:**

```
input array :  ['GEEKS' 'for' 'Geeks']
output array : [False False  True]

```