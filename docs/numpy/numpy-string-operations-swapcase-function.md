# numpy 字符串操作| swapcase()功能

> 原文:[https://www . geesforgeks . org/numpy-string-operations-swap base-function/](https://www.geeksforgeeks.org/numpy-string-operations-swapcase-function/)

**`numpy.core.defchararray.swapcase(arr)`** 函数按元素返回字符串的副本，其中大写字符转换为小写字符，小写字符转换为大写字符。

> **语法:** numpy.char.swapcase(arr)
> 
> **参数:**
> **arr:**【array _ like】输入可能是字符串或 unicode 的数组。
> 
> **返回:**【ndarray】输出字符串或 unicode 的低位数组，具体取决于输入类型。

**代码#1:**

```py
# Python Program explaining
# numpy.char.swapcase() function 

import numpy as geek 

in_arr = geek.array(['P4Q R', '4q Rp', 'Q Rp4', 'rp4q'])
print ("input array : ", in_arr)

out_arr = geek.char.swapcase(in_arr)
print ("output swapcasecased array :", out_arr)
```

**Output:**

```py
input array :  ['P4Q R' '4q Rp' 'Q Rp4' 'rp4q']
output swapcasecased array : ['p4q r' '4Q rP' 'q rP4' 'RP4Q']

```

**代码#2:**

```py
# Python Program explaining
# numpy.char.swapcase() function 

import numpy as geek 

in_arr = geek.array(['Geeks', 'For', 'Geeks'])

print ("input array : ", in_arr)

out_arr = geek.char.swapcase(in_arr)
print ("output swapcasecased array :", out_arr )
```

**Output:**

```py
input array :  ['Geeks' 'For' 'Geeks']
output swapcasecased array : ['gEEKS' 'fOR' 'gEEKS']

```