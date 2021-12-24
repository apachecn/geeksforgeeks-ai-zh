# numpy 字符串操作|上()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-upper-function/](https://www.geeksforgeeks.org/numpy-string-operations-upper-function/)

**`numpy.core.defchararray.upper(arr)` :** 函数用于返回元素被转换为大写的数组。

> **参数:**
> **arr:**【array _ like】输入可能是字符串或 unicode 的数组。
> 
> **返回:**【ndarray】输出字符串或 unicode 的高位数组，具体取决于输入类型。

**代码#1:**

```py
# Python Program explaining
# numpy.char.upper() function 

import numpy as geek 

in_arr = geek.array(['p4q r', '4q rp', 'q rp4', 'rp4q'])
print ("input array : ", in_arr)

out_arr = geek.char.upper(in_arr)
print ("output uppercased array :", out_arr)
```

**Output:**

```py
input array :  ['p4q r' '4q rp' 'q rp4' 'rp4q']
output uppercased array : ['P4Q R' '4Q RP' 'Q RP4' 'RP4Q']

```

**代码#2:**

```py
# Python Program explaining
# numpy.char.upper() function 

import numpy as geek 

in_arr = geek.array(['geeks', 'for', 'geeks'])

print ("input array : ", in_arr)

out_arr = geek.char.upper(in_arr)
print ("output uppercased array :", out_arr )
```

**Output:**

```py
input array :  ['geeks' 'for' 'geeks']
output uppercased array : ['GEEKS' 'FOR' 'GEEKS']

```