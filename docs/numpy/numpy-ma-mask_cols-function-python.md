# numpy.ma.mask_cols()函数| Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ma-mask _ cols-function-python/

在这个 **`numpy.ma.mask_cols()`** 函数中，屏蔽包含屏蔽值的 2D 数组的列。这个函数是 mask_rowcols 轴等于 1 的快捷方式。

> **语法:** numpy.ma.mask_cols(arr，axis = None)
> 
> **参数:**
> **arr :** 【阵 _ 象，掩克阵】该阵要掩。
> **轴:**【int，可选】执行操作的轴。默认值为无。
> 
> **返回:**【maskearray】输入数组的修改版本。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.mask_cols() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.zeros((3, 3), dtype = int)
arr[1, 1] = 1

arr = ma.masked_equal(arr, 1)

gfg = ma.mask_cols(arr)

print (gfg)
```

**输出:**

```py
[[0 -- 0]
 [0 -- 0]
 [0 -- 0]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.mask_cols() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.zeros((4, 4), dtype = int)
arr[2, 2] = 1

arr = ma.masked_equal(arr, 1)

gfg = ma.mask_cols(arr)

print (gfg)
```

**输出:**

```py
[[0 0 -- 0]
 [0 0 -- 0]
 [0 0 -- 0]
 [0 0 -- 0]]

```