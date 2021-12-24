# numpy 字符串操作| title()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-title-function/](https://www.geeksforgeeks.org/numpy-string-operations-title-function/)

**`numpy.core.defchararray.title(arr)` :** 函数用于返回字符串或 unicode 的元素标题。标题大小写以大写字符开头，其余所有大小写字符都是小写。

> **参数:**
> **arr:**【array _ like】输入可能是字符串或 unicode 的数组。
> 
> **根据输入类型，返回字符串或 unicode 的输出数组。**

**代码#1:**

```py
# Python Program explaining
# numpy.char.title() function 

import numpy as geek 

in_arr = geek.array(['p4q r', '4q rp', 'q rp4', 'rp4q'])
print ("input array : ", in_arr)

out_arr = geek.char.title(in_arr)
print ("output titled array :", out_arr)
```

**Output:**

```py
input array :  ['p4q r' '4q rp' 'q rp4' 'rp4q']
output titled array : ['P4Q R' '4Q Rp' 'Q Rp4' 'Rp4Q']

```

**代码#2:**

```py
# Python Program explaining
# numpy.char.title() function 

import numpy as geek 

in_arr = geek.array(['geeks', 'for', 'geeks'])

print ("input array : ", in_arr)

out_arr = geek.char.title(in_arr)
print ("output titled array :", out_arr )
```

**Output:**

```py
input array :  ['geeks' 'for' 'geeks']
output titled array : ['Geeks' 'For' 'Geeks']

```