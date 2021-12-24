# numpy . undeflot _ index()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-under find _ index-function-python/](https://www.geeksforgeeks.org/numpy-unravel_index-function-python/)

**`numpy.unravel_index()`** 函数将平面索引或平面索引数组转换为坐标数组的元组。

> **语法:**numpy . undeflot _ index(indexes，shape，order = 'C')
> **参数:**
> **indexes:**【array _ like】一个整数数组，其元素是维度形状数组的扁平版本的索引。
> **形状:**【整数元组】用于展开索引的数组的形状。
> **顺序:** [{'C '，' F'}，可选]确定多索引应视为以行为主(C 风格)还是列为主(Fortran 风格)的顺序进行索引。
> 
> **返回:**【数组的元组】元组中的每个数组都具有与索引数组相同的形状。

**代码#1 :**

```
# Python program explaining
# numpy.unravel_index() function

# importing numpy as geek 
import numpy as geek

gfg = geek.unravel_index([22, 41, 37], (7, 6))

print(gfg) 
```

**输出:**

```
(array([3, 6, 6]), array([4, 5, 1]))

```

**代码#2 :**

```
# Python program explaining
# numpy.unravel_index() function

# importing numpy as geek 
import numpy as geek

gfg = geek.unravel_index([22, 41, 37], (7, 6), order = 'F')

print(gfg) 
```

**输出:**

```
(array([1, 6, 2]), array([3, 5, 5]))

```