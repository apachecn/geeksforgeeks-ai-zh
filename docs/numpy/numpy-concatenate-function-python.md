# numpy.concatenate()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-concatenate-function-python/](https://www.geeksforgeeks.org/numpy-concatenate-function-python/)

**`numpy.concatenate()`** 函数沿着现有轴连接一系列数组。

> **语法:** numpy.concatenate((arr1，arr2，…)，axis=0，out=None)
> **参数:**
> **arr1，arr2，…:**【array _ like 的序列】数组必须具有相同的形状，但与 axis 对应的维度除外。
> **轴:**【int，可选】阵列将沿其连接的轴。如果轴为“无”，数组在使用前会被展平。默认值为 0。
> **出:**【n 数组，可选】如果提供，目的地放置结果。形状必须正确，与未指定 out 参数时 concatenate 返回的形状相匹配。
> **返回:**【n 数组】连接的数组。

**代码#1 :**

```py
# Python program explaining
# numpy.concatenate() function

# importing numpy as geek 
import numpy as geek

arr1 = geek.array([[2, 4], [6, 8]])
arr2 = geek.array([[3, 5], [7, 9]])

gfg = geek.concatenate((arr1, arr2), axis = 0)

print (gfg)
```

**输出:**

```py
[[2 4]
 [6 8]
 [3 5]
 [7 9]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.concatenate() function

# importing numpy as geek 
import numpy as geek

arr1 = geek.array([[2, 4], [6, 8]])
arr2 = geek.array([[3, 5], [7, 9]])

gfg = geek.concatenate((arr1, arr2), axis = 1)

print (gfg)
```

**输出:**

```py
[[2 4 3 5]
 [6 8 7 9]]

```

**代码#3 :**

```py
# Python program explaining
# numpy.concatenate() function

# importing numpy as geek 
import numpy as geek

arr1 = geek.array([[2, 4], [6, 8]])
arr2 = geek.array([[3, 5], [7, 9]])

gfg = geek.concatenate((arr1, arr2), axis = None)

print (gfg)
```

**输出:**

```py
[2 4 6 8 3 5 7 9]

```