# numpy.ma.where()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-ma-where-function-python/](https://www.geeksforgeeks.org/numpy-ma-where-function-python/)

**`numpy.ma.where()`** 函数根据条件返回一个带有 x 或 y 元素的屏蔽数组。

> **语法:** numpy.ma.where(条件，x，y)
> 
> **参数:**
> **条件:**【array _ like，bool】Where True，yield x，否则 yield y.
> **x，y:**【array _ like，可选】可供选择的值。x、y 和条件需要可以扩展到某种形状。
> 
> **Return:**【maskedArray】一个被屏蔽的数组，其中条件被屏蔽的地方有被屏蔽的元素，条件为 True 的地方有来自 x 的元素，其他地方有来自 y 的元素。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.where() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma

x = geek.ma.array(geek.arange(4.).reshape(2, 2), 
                        mask =[[0, 1], [1, 0]])

gfg = geek.ma.where(x > 5, x, -3.1416)

print (gfg)
```

**输出:**

```py
[[-3.1416 --]
 [-- -3.1416]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.where() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma

x = geek.ma.array(geek.arange(9.).reshape(3, 3), 
       mask =[[0, 1, 0], [1, 0, 1], [0, 1, 0]])

gfg = geek.ma.where(x > 5, x, -3.1416)

print (gfg)
```

**输出:**

```py
[[-3.1416 -- -3.1416]
 [-- -3.1416 --]
 [6.0 -- 8.0]]

```