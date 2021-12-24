# Python 中 numpy.ma.compress_rowcols()函数

> 原文:[https://www . geeksforgeeks . org/numpy-ma-compress _ rowcols-python 中的函数/](https://www.geeksforgeeks.org/numpy-ma-compress_rowcols-function-in-python/)

**numpy . ma . compress _ row cols()**函数抑制二维数组中包含掩码值的行和列。
使用轴参数选择抑制行为:

*   如果轴为“无”，则行和列都被抑制。
*   如果轴为 0，则仅抑制行。
*   如果轴为 1 或-1，则仅抑制列。

> **语法:**numpy . ma . compress _ row cols(arr，axis = None)
> 
> **参数:**
> **arr:**【array _ like，MaskedArray】此参数保存要操作的数组。该数组必须是 2D 数组。如果没有数组元素被屏蔽，arr 将被解释为一个屏蔽数组，屏蔽设置为 nomask。
> **轴:**【int，可选】执行操作的轴。默认值为无。
> 
> **返回:**返回压缩后的数组。

**代码#1:**

## 蟒蛇 3

```py
# Python program explaining
# numpy.ma.compress_rowcols() function

# importing numpy as geek
import numpy as geek

arr = geek.ma.array(geek.arange(6).reshape(2, 3),
                    mask=[[1, 0, 0], [0, 0, 0]])

gfg = geek.ma.compress_rowcols(arr)

print(gfg)
```

**输出:**

```py
[[4 5]]

```

**代码#2:**

## 蟒蛇 3

```py
# Python program explaining
# numpy.ma.compress_rowcols() function

# importing numpy as geek
import numpy as geek

arr = geek.ma.array(geek.arange(6).reshape(2, 3),
                    mask=[[1, 0, 0], [0, 0, 0]])

gfg = geek.ma.compress_rowcols(arr, 1)

print(gfg)
```

**输出:**

```py
[[1 2]
 [4 5]]

```