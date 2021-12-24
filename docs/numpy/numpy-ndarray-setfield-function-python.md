# num py ndaarray . set field()函数| Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ndaarray-setfield-function-python/

**`numpy.ndarray.setfield()`** 函数将值放入由数据类型定义的字段中的指定位置。将 val 放入由数据类型定义的字段中，并将起始偏移字节放入该字段中。

> **语法:**num py . ndaarray . set field(val，dtype，offset=0)
> 
> **参数:**
> **值:**【对象】要放置在字段中的值。
> **数据类型:**【数据类型对象】放置 val 的字段的数据类型。
> **偏移量:**【int，可选】字段中放置 val 的字节数。
> 
> **返回:**无。

**代码#1 :**

```
# Python program explaining
# numpy.ndarray.setfield() function

# importing numpy as geek 
import numpy as geek 

arr = geek.eye(4)

arr.setfield(4, geek.int32)
gfg = arr.getfield(geek.int32)

print(gfg)
```

**输出:**

```
[[4 4 4 4]
 [4 4 4 4]
 [4 4 4 4]
 [4 4 4 4]]

```

**代码#2 :**

```
# Python program explaining
# numpy.ndarray.setfield() function

# importing numpy as geek 
import numpy as geek 

arr = geek.eye(2)

arr.setfield(2, geek.int32)
gfg = arr.getfield(geek.int32)

print(gfg)
```

**输出:**

```
[[2 2]
 [2 2]]

```