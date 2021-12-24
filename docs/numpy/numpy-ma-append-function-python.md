# numpy.ma.append()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-append-function-python/](https://www.geeksforgeeks.org/numpy-ma-append-function-python/)

**`numpy.ma.append()`** 函数将值追加到数组的末尾。

> **语法:** numpy.ma.append(arr1，arr2，axis = None)
> **参数:**
> **arr 1:**【array _ like】值被追加到该数组的副本中。
> **arr 2:**【array _ like】值被追加到该数组的副本中。如果未指定轴，arr2 可以是任何形状，并将在使用前展平。否则，它必须是正确的形状。
> **轴:**【int，可选】附加值的轴。
> **返回:**【maskearray】arr 1 的副本，arr2 附加在轴上。如果轴为“无”，则结果为展平数组。

**代码#1 :**

```
# Python program explaining
# numpy.ma.append() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr1 = ma.masked_values([1, 2, 3], 3)
arr2 = ma.masked_values([[4, 5, 6], [7, 8, 9]], 8)

gfg = ma.append(arr1, arr2)

print (gfg)
```

**输出:**

```
[1 2 -- 4 5 6 7 -- 9]

```

**代码#2 :**

```
# Python program explaining
# numpy.ma.append() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr1 = ma.masked_values([1, 2, 3, 4], 2)
arr2 = ma.masked_values([[5, 6, 7], [8, 9, 10]], 8)

gfg = ma.append(arr1, arr2)

print (gfg)
```

**输出:**

```
[1 -- 3 4 5 6 7 -- 9 10]

```