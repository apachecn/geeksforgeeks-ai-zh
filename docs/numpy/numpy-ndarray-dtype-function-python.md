# num py . ndaarray . dttype()函数–python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ndaarray-dtype-function-python/

**`numpy.ndarray.dtype()`** 函数返回数组元素的数据类型。

> **语法:**num py . ndaarray . dttype()
> 
> **参数:**无
> 
> **返回:**【numpy dtype 对象】返回数组元素的数据类型。

**代码#1 :**

```
# Python program explaining
# numpy.ndarray.dtype() function

# importing numpy as geek 
import numpy as geek 

arr = geek.array([[0, 1], [2, 3]])

gfg = arr.dtype

print (gfg)
```

**输出:**

```
int64
```

**代码#2 :**

```
# Python program explaining
# numpy.ndarray.dtype() function

# importing numpy as geek 
import numpy as geek 

arr = geek.array([  0.,  1.,  2.])

gfg = arr.dtype

print (gfg)
```

**输出:**

```
float64

```