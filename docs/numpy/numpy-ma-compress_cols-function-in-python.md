# Python 中 numpy.ma.compress_cols()函数

> 原文:[https://www . geesforgeks . org/numpy-ma-compress _ cols-function-in-python/](https://www.geeksforgeeks.org/numpy-ma-compress_cols-function-in-python/)

**先决条件:**T2

此 numpy 内置函数抑制二维数组中包含掩码值的整列。

> **语法:** numpy.ma.compress_cols(arr)
> 
> **参数:**
> 
> **arr:**T2【array _ like，maske array】
> 
> 1.  此参数保存要操作的数组。
> 2.  该数组必须是 2D 数组。
> 3.  如果没有数组元素被屏蔽，arr 将被解释为一个屏蔽数组，屏蔽设置为 nomask。
>     
> 
> **返回:**返回压缩后的数组。

下面是上述功能的实现。

**例 1:**

## 蟒蛇 3

```
# importing numpy as geek
import numpy as geek

# defining an array with mask
arr = geek.ma.array(geek.arange(6).reshape(2, 3),
                    mask=[[1, 0, 0], [0, 0, 0]])

# applying mask to array elements
gfg = geek.ma.compress_cols(arr)

print(gfg)
```

**输出:**

```
[[1 2]
 [4 5]]

```

**例 2:**

## 蟒蛇 3

```
# importing numpy as geek
import numpy as geek

# defining array
arr = geek.ma.array(geek.arange(9).reshape(3, 3), mask=[
                    [1, 0, 0], [1, 0, 0], [0, 0, 0]])

# applying mask to array elements
gfg = geek.ma.compress_cols(arr)

print(gfg)
```

**输出:**

```
[[1 2]
 [4 5]
 [7 8]]

```