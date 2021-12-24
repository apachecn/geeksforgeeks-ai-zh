# numpy . root()函数–Python

> 原文:[https://www.geeksforgeeks.org/numpy-roots-function-python/](https://www.geeksforgeeks.org/numpy-roots-function-python/)

**`numpy.roots()`** 函数返回一个多项式的根，其系数在 p 中给出。秩为 1 的数组 p 中的值是多项式的系数。如果 p 的长度是 n+1，那么多项式的描述如下:p[0]* x * * n+p[1]* x * *(n-1)+…+p[n-1]* x+p[n]

> **语法:**numpy . root(p)
> 
> **参数:**
> **p:**【array _ like】多项式系数的 Rank-1 数组。
> 
> **返回:**【ndarray】包含多项式根的数组。

**代码#1 :**

```
# Python program explaining
# numpy.roots() function

# importing numpy as geek 
import numpy as geek 

p = [1, 2, 3]

gfg = geek.roots(p)

print (gfg)
```

**输出:**

```
[-1.+1.41421356j -1.-1.41421356j]

```

**代码#2 :**

```
# Python program explaining
# numpy.roots() function

# importing numpy as geek 
import numpy as geek 

p = [3.2, 2, 1]

gfg = geek.roots(p)

print (gfg)
```

**输出:**

```
[-0.3125+0.46351241j -0.3125-0.46351241j]

```