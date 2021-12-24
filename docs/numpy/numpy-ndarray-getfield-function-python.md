# num py ndaarray . getfield()函数| Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ndaarray-getfield-function-python/

**`numpy.ndarray.getfield()`** 函数返回给定数组的某个字段作为某个类型。

> **语法:**num py . ndaarray . getfield(dttype，offset=0)
> 
> **参数:**
> **数据类型:**【字符串或数据类型】视图的数据类型大小不能大于数组本身的大小。
> **偏移量:**【int】开始元素视图前要跳过的字节数。
> 
> **返回:**返回给定数组的某个字段作为某个类型。

**代码#1 :**

```
# Python program explaining
# numpy.ndarray.getfield() function

# importing numpy as geek 
import numpy as geek 

x = geek.diag([1.+1.j]*2)

gfg = x.getfield(geek.float64)

print(gfg)
```

**输出:**

```
[[ 1\.  0.]
 [ 0\.  1.]]

```

**代码#2 :**

```
# Python program explaining
# numpy.ndarray.getfield() function

# importing numpy as geek 
import numpy as geek 

x = geek.diag([2.+2.j]*2)

gfg = x.getfield(geek.float64, offset = 8)

print(gfg)
```

**输出:**

```
[[ 2\.  0.]
 [ 0\.  2.]]

```