# Python 中 numpy.ma.ediff1d()函数

> 原文:[https://www . geesforgeks . org/numpy-ma-ediff 1d-python 中的函数/](https://www.geeksforgeeks.org/numpy-ma-ediff1d-function-in-python/)

**numpy.ma.ediff1d()** 函数返回数组中连续元素之间的差异。

> **语法:** numpy.ma.ediff1d(arr，to_end =无，to_begin =无)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **to _ end:**【array _ like，可选】要追加到返回差异末尾的数字。
> **to _ begin:**【array _ like，可选】要在返回的差异开头前置的数字。
> 
> **Return :** 返回数组中连续元素之间的差异。

**代码#1:**

## 蟒蛇 3

```py
# Python program explaining
# numpy.ma.ediff1d() function

# importing numpy as geek
import numpy as geek

arr = geek.array([3, 5, 8, 4, 12])

gfg = geek.ma.ediff1d(arr)

print(gfg)
```

**输出:**

```py
[ 2  3 -4  8]

```

**代码#2:**

## 蟒蛇 3

```py
# Python program explaining
# numpy.ma.ediff1d() function

# importing numpy as geek
import numpy as geek

arr = geek.array([3, 5, 8, 4, 12])

gfg = geek.ma.ediff1d(arr, to_begin=geek.array([-23, 0]), to_end=25)

print(gfg)
```

**输出:**

```py
[-23 0 2 3 -4 8 25]

```