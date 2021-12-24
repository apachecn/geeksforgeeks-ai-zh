# numpy 字符串操作| lower()功能

> 原文:[https://www . geesforgeks . org/numpy-string-operations-low-function/](https://www.geeksforgeeks.org/numpy-string-operations-lower-function/)

**`numpy.core.defchararray.lower(arr)`** 函数用于返回一个元素转换为小写的数组。

> **参数:**
> **arr:**【array _ like】输入可能是字符串或 unicode 的数组。
> 
> **返回:**【ndarray】输出字符串或 unicode 的低位数组，具体取决于输入类型。

**代码#1:**

```
# Python Program explaining
# numpy.char.lower() function 

import numpy as geek 

in_arr = geek.array(['P4Q R', '4Q RP', 'Q RP4', 'RP4Q'])
print ("input array : ", in_arr)

out_arr = geek.char.lower(in_arr)
print ("output lowercased array :", out_arr)
```

**Output:**

```
input array :  ['P4Q R' '4Q RP' 'Q RP4' 'RP4Q']
output lowercased array : ['p4q r' '4q rp' 'q rp4' 'rp4q']

```

**代码#2:**

```
# Python Program explaining
# numpy.char.lower() function 

import numpy as geek 

in_arr = geek.array(['GEEKS', 'FOR', 'GEEKS'])

print ("input array : ", in_arr)

out_arr = geek.char.lower(in_arr)
print ("output lowercased array :", out_arr )
```

**Output:**

```
input array :  ['GEEKS' 'FOR' 'GEEKS']
output lowercased array : ['geeks' 'for' 'geeks']

```