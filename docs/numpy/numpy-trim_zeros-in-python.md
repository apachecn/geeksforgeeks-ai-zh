# Python 中的 numpy.trim_zeros()

> 原文:[https://www.geeksforgeeks.org/numpy-trim_zeros-in-python/](https://www.geeksforgeeks.org/numpy-trim_zeros-in-python/)

*numpy . trim _ zeross*函数用于修剪一维数组或序列的前导和/或尾随零。

> **语法:** numpy.trim_zeros(arr，trim)
> 
> **参数:**
> **arr :** 一维数组或序列
> **trim :** trim 是一个可选参数，默认值为‘FB’(正面和背面)我们可以选择‘f’(正面)或‘b’代表背面。
> 
> **返回:**修剪后的一维数组或序列(根据用户的选择不带前导和/或尾随零)

**代码 1:**

```
import numpy as geek 

gfg = geek.array((0, 0, 0, 0, 1, 5, 7, 0, 6, 2, 9, 0, 10, 0, 0))

# without trim parameter
# returns an array without leading and trailing zeros 

res = geek.trim_zeros(gfg)
print(res)
```

```
Output :array([1, 5, 7, 0, 6, 2, 9, 0, 10])

```

**代码 2:**

```
import numpy as geek 
gfg = geek.array((0, 0, 0, 0, 1, 5, 7, 0, 6, 2, 9, 0, 10, 0, 0))

# without trim parameter
# returns an array without any leading  zeros 

res = geek.trim_zeros(gfg, 'f')
print(res)
```

```
Output :array([1, 5, 7, 0, 6, 2, 9, 0, 10, 0, 0])

```

**代码 3:**

```
import numpy as geek 
gfg = geek.array((0, 0, 0, 0, 1, 5, 7, 0, 6, 2, 9, 0, 10, 0, 0))

# without trim parameter
# returns an array without any trailing  zeros 

res = geek.trim_zeros(gfg, 'b')
print(res)
```

```
Output :array([0, 0, 0, 0, 1, 5, 7, 0, 6, 2, 9, 0, 10])

```