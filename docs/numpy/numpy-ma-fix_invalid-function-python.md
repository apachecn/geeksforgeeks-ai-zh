# numpy.ma.fix_invalid()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-fix _ invalid-function-python/](https://www.geeksforgeeks.org/numpy-ma-fix_invalid-function-python/)

**`numpy.ma.fix_invalid()`** 函数返回输入用无效数据屏蔽并由填充值代替。其中无效数据表示 nan、inf 等的值。

> **语法:** numpy.ma.fix_invalid(arr，mask = False，copy = True，fill_value = None)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **掩码:**【序列，可选】必须可转换为与数据形状相同的布尔数组。True 表示屏蔽的数据。
> **副本:**【bool，可选】是使用副本(True)还是就地修复副本(False)。默认值为真。
> **fill_value :** 【标量，可选】用于修复无效数据的值。默认值为无，在这种情况下使用 arr.fill_value。
> 
> **返回:**【屏蔽数组】输入数组中无效条目被修复。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.fix_invalid() function

# importing numpy as geek 
import numpy as geek 

arr = geek.ma.array([1., -1, geek.nan, geek.inf],
                              mask =[1] + [0]*3)

gfg = geek.ma.fix_invalid(arr)

print (gfg)
```

**输出:**

```py
[-- -1.0 -- --]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.fix_invalid() function

# importing numpy as geek 
import numpy as geek 

arr = geek.ma.array([1., -1, geek.nan,
                    geek.inf, -1, geek.nan],
                          mask =[1] + [0]*5)

gfg = geek.ma.fix_invalid(arr)

print (gfg)
```

**输出:**

```py
[-- -1.0 -- -- -1.0 --]

```