# numpy.ravel_multi_index()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ravel _ multi _ index-function-python/](https://www.geeksforgeeks.org/numpy-ravel_multi_index-function-python/)

**`numpy.ravel_multi_index()`** 函数将一组索引数组转换为一组平面索引，对多索引应用边界模式。

> **语法:**numpy . ravel _ multi _ index(multi _ index，dims，mode = 'raise '，order = 'C)
> **参数:**
> **multi_index :** 【数组的元组 _like】整数数组的元组，每个维度一个数组。
> **dims :** 【整数元组】数组的形状，多索引中的索引应用于该数组。
> **模式:** [{ '提升'，'环绕'，'剪辑' }，可选]指定如何处理越界索引。可以指定一种模式或一组模式，每个索引一种模式。
> “提升”–引发错误(默认)
> “环绕”–环绕
> “剪辑”–剪辑到范围
> 在“剪辑”模式下，通常会环绕的负索引将改为剪辑到 0。
> **顺序:** [{'C '，' F'}，可选]确定多索引应视为以行为主(C 风格)还是列为主(Fortran 风格)的顺序进行索引。
> 
> **返回:**【ndarray】将索引数组转换为维度数组 dims 的扁平版本。

**代码#1 :**

```py
# Python program explaining
# numpy.ravel_multi_index() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[3, 6, 6], [4, 5, 1]])

gfg = geek.ravel_multi_index(arr, (7, 6))

print(gfg) 
```

**输出:**

```py
[22 41 37]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ravel_multi_index() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[3, 6, 6], [4, 5, 1]])

gfg = geek.ravel_multi_index(arr, (7, 6), order = 'F')

print(gfg) 
```

**输出:**

```py
[31 41 13]

```

**代码#3 :**

```py
# Python program explaining
# numpy.ravel_multi_index() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[3, 6, 6], [4, 5, 1]])

gfg = geek.ravel_multi_index(arr, (7, 6), mode = 'clip')

print(gfg) 
```

**输出:**

```py
[22 41 37]

```