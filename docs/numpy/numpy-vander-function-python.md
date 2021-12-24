# numpy.vander()函数| Python

> 原文:[https://www.geeksforgeeks.org/numpy-vander-function-python/](https://www.geeksforgeeks.org/numpy-vander-function-python/)

**`numpy.vander()`** 函数用于生成范德蒙矩阵。

> **语法:** numpy.vander(arr，N = None，递增= False)
> **参数:**
> **arr:**【array _ like】一维输入数组。
> **N:**【int，可选】输出中的列数。如果未指定 N，则返回一个方形数组(N = len(x))。
> **递增:**【布尔，可选】列幂的顺序。如果为真，功率从左向右增加，如果为假(默认值)，功率反向。
> **返回:**【ndarray】dVandermonde 矩阵。如果递增是假的，第一列是 x^(N-1)，第二列是 x^(N-2)等等。如果增加是真的，那么列是 x^0，x^1，…，x^(N-1).

**代码#1 :**

```
# Python program explaining
# numpy.vander() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([1, 2, 3, 4, 5])

gfg = geek.vander(arr)

print (gfg)
```

**输出:**

```
[[  1   1   1   1   1]
 [ 16   8   4   2   1]
 [ 81  27   9   3   1]
 [256  64  16   4   1]
 [625 125  25   5   1]]

```

**代码#2 :**

```
# Python program explaining
# numpy.vander() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([1, 2, 3, 4, 5])
N = 3

gfg = geek.vander(arr, N)

print (gfg)
```

**输出:**

```
[[ 1  1  1]
 [ 4  2  1]
 [ 9  3  1]
 [16  4  1]
 [25  5  1]]

```

**代码#3 :**

```
# Python program explaining
# numpy.vander() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([1, 2, 3, 4, 5])

gfg = geek.vander(arr, increasing = True)

print (gfg)
```

**输出:**

```
[[  1   1   1   1   1]
 [  1   2   4   8  16]
 [  1   3   9  27  81]
 [  1   4  16  64 256]
 [  1   5  25 125 625]]

```