# numpy.broadcast_to()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-broadcast _ to-function-python/](https://www.geeksforgeeks.org/numpy-broadcast_to-function-python/)

numpy.broadcast_to()函数将数组广播到新的形状。

> **语法:** numpy.broadcast_to(数组，形状，subok = False)
> 
>  **参数:
> 
> 数组:[array_liket]要广播的数组。
> 
> 形状:[元组]所需数组的形状。
> 
> subok : [bool，可选]如果为 True，则将传递子类，否则默认情况下，返回的数组将被强制为基类数组。
> 
> **返回:**【数组】输出数组。**

**代码#1:**

## **蟒蛇 3**

```
# Python program explaining
# numpy.broadcast_to() function

# importing numpy as geek
import numpy as geek

arr = geek.array([1, 2, 3, 4])

gfg = geek.broadcast_to(arr, (4, 4))

print(gfg)
```

**输出:**

> **[[1 2 3 4]**
> 
> **[1 2 3 4]**
> 
> **[1 2 3 4]**
> 
> **[1 2 3 4]]**

**代码#2:**

## **蟒蛇 3**

```
# Python program explaining
# numpy.broadcast_to() function

# importing numpy as geek
import numpy as geek

arr = geek.array([1, 2, 3, 4, 5])

gfg = geek.broadcast_to(arr, (5, 5))

print(gfg)
```

**输出:**

> **[[1 2 3 4 5]**
> 
> **[1 2 3 4 5]**
> 
> **[1 2 3 4 5]**
> 
> **[1 2 3 4 5]**
> 
> **[1 2 3 4 5]]**