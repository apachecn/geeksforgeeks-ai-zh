# numpy.ma.make_mask()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-make _ mask-function-python/](https://www.geeksforgeeks.org/numpy-ma-make_mask-function-python/)

**numpy.ma.make_mask()** 函数用于从数组创建布尔掩码。
这个函数可以接受任何可以转换成整数的序列，或者称之为 nomask。它不要求内容必须是 0 和 1，0 的值被解释为假，其他都是真。返回 m 作为布尔掩码。

> **语法:** numpy.ma.make_mask(m，copy = False，shrink = True，dtype = bool )
> **参数:**
> **arr:**【array _ like】电位掩码。
> **副本:**【bool，可选】是返回 m 的副本(True)还是 m 本身的副本(False)。
> **收缩:**【bool，可选】如果 m 的所有值都为 False，是否将 m 收缩为 nomask。
> **数据类型:**【数据类型，可选】输出掩码的数据类型。默认情况下，输出掩码的数据类型为掩码类型(bool)。
> **返回:**【ndarray】一个从 m.
> 派生的布尔掩码

**代码#1 :**

## 蟒蛇 3

```
# Python program explaining
# numpy.ma.make_mask() function

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

m = [1, 1, 0, 1]

gfg = ma.make_mask(m)

print (gfg)
```

**输出:**

```
[ True  True False  True]
```

**代码#2 :**

## 蟒蛇 3

```
# Python program explaining
# numpy.ma.make_mask() function

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

m = [2, -3, 0, 1]

gfg = ma.make_mask(m)

print (gfg)
```

**输出:**

```
[ True  True False  True]
```

**代码#3 :**

## 蟒蛇 3

```
# Python program explaining
# numpy.ma.make_mask() function

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

m = [True, True, True, False]

gfg = ma.make_mask(m)

print (gfg)
```

**输出:**

```
[ True  True  True False]
```