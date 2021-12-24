# numpy . indexs()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-indexs-function-python/](https://www.geeksforgeeks.org/numpy-indices-function-python/)

**`numpy.indices()`** 函数返回一个代表网格索引的数组。计算一个数组，其中子数组包含仅沿相应轴变化的索引值 0，1，…。

> **语法:**numpy . indexs(维度，数据类型，稀疏= False)
> 
> **参数:**
> **尺寸:**【ints 序列】网格的形状。
> **数据类型:**【数据类型，可选】结果的数据类型。
> **稀疏:**【布尔，可选】返回网格的稀疏表示，而不是密集表示。默认值为假。
> 
> **返回:**【数组或数组元组】
> 如果稀疏为假:
> 返回一个网格索引数组，grid.shape = (len(dimensions)，)+ tuple(dimensions)。
> 
> 如果稀疏为真:
> 返回数组的元组，带有网格[i]。形状= (1，…，1，尺寸[i]，1，…，1)，尺寸[i]在第 I 个位置

**代码#1 :**

```py
# Python program explaining
# numpy.indices() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.indices((2, 3))

print (gfg)
```

**输出:**

```py
[[[0 0 0]
  [1 1 1]]

 [[0 1 2]
  [0 1 2]]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.indices() function

# importing numpy as geek 
import numpy as geek 

grid = geek.indices((2, 3))
gfg = grid[1]

print (gfg)
```

**输出:**

```py
[[0 1 2]
 [0 1 2]]

```