# numpy.ix_()函数| Python

> 原文:[https://www.geeksforgeeks.org/numpy-ix_-function-python/](https://www.geeksforgeeks.org/numpy-ix_-function-python/)

**`numpy.ix_()`** 函数从多个序列构建一个开放网格。该函数采用 N 个一维序列，并返回 N 个输出，每个输出有 N 个维度，这样，除了一个维度之外，所有维度中的形状都是 1，而具有非单位形状值的维度在所有 N 个维度中循环。

> **语法:** numpy.ix_(args)
> **参数:**
> **args:**【1-D 序列】每个序列应为整数或布尔类型。
> **返回:**【数组元组】N 个数组，每个数组 N 维，N 为输入序列数。这些阵列一起形成一个开放的网格。

**代码#1 :**

```py
# Python program explaining
# numpy.ix_() function

# importing numpy as geek 
import numpy as geek

gfg = geek.ix_([0, 1], [2, 4])

print (gfg)
```

**输出:**

```py
(array([[0],
       [1]]), array([[2, 4]]))

```

**代码#2 :**

```py
# Python program explaining
# numpy.ix_() function

# importing numpy as geek 
import numpy as geek

arr = geek.arange(10).reshape(2, 5)
print("Initial array : \n", arr) 

ixgrid = geek.ix_([0, 1], [2, 4])

print("New array : \n", arr[ixgrid]) 
```

**输出:**

```py
Initial array : 
 [[0 1 2 3 4]
 [5 6 7 8 9]]
New array : 
 [[2 4]
 [7 9]]

```