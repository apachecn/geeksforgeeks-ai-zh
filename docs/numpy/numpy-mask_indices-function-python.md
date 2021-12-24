# numpy . mask _ indexs()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-mask _ indexs-function-python/](https://www.geeksforgeeks.org/numpy-mask_indices-function-python/)

**`numpy.mask_indices()`** 函数返回索引以访问(n，n)个数组，给定一个屏蔽函数。

> **语法:**numpy . mask _ indexs(n，mask_func，k = 0)
> **参数:**
> **n:**【int】返回的索引对于访问 shape (n，n)数组有效。
> **mask_func :** 【可调用】调用签名与 triu、tril 类似的函数。
> **k :** 【标量】传递给 mask_func 的可选参数。
> **返回:**【数组元组】对应于 mask _ func(NP . one((n，n))，k)为真的位置的 n 个数组索引。

**代码#1 :**

```
# Python program explaining
# numpy.mask_indices() function

# importing numpy as geek 
import numpy as geek

gfg = geek.mask_indices(3, geek.triu)

print (gfg)
```

**输出:**

```
(array([0, 0, 0, 1, 1, 2]), array([0, 1, 2, 1, 2, 2]))

```

**代码#2 :**

```
# Python program explaining
# numpy.mask_indices() function

# importing numpy as geek 
import numpy as geek

gfg = geek.mask_indices(3, geek.triu, 1)

print (gfg)
```

**输出:**

```
(array([0, 0, 1]), array([1, 2, 2]))

```