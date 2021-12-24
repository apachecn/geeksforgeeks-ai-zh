# Python 中的 numpy.apply_over_axes()

> 原文:[https://www.geeksforgeeks.org/numpy-apply_over_axes-python/](https://www.geeksforgeeks.org/numpy-apply_over_axes-python/)

**numpy.apply_over_axes()** 在数组中的多个轴上重复应用一个函数。

**语法:**

```py
numpy.apply_over_axes(func, array, axes)
```

**参数:**

```py
1d_func  : the required function to perform over 1D array. It can only be applied in 
         1D slices of input array and that too along a particular axis. 
axis     : required axis along which we want input array to be sliced
array    : Input array to work on 
*args    : Additional arguments to 1D_function 
**kwargs : Additional arguments to 1D_function  
```

**返回:**

```py
The output array. Shape of the output array can be different depending on whether func 
changes the shape of its output with respect to its input.
```

**代码 1 :**

## 计算机编程语言

```py
# Python Program illustrating
# apply_over_axis() in NumPy

import numpy as geek

# Using a 3D array
geek_array = geek.arange(16).reshape(2, 2, 4)
print("geek array  :\n", geek_array)

# Applying pre-defined sum function over the axis of 3D array
print("\nfunc sum : \n ", geek.apply_over_axes(geek.sum, geek_array, [1, 1, 0]))

# Applying pre-defined min function over the axis of 3D array
print("\nfunc min : \n ", geek.apply_over_axes(geek.min, geek_array, [1, 1, 0]))
```

**输出:**

```py
geek array  :
 [[[ 0  1  2  3]
  [ 4  5  6  7]]

 [[ 8  9 10 11]
  [12 13 14 15]]]

func sum : 
  [[[24 28 32 36]]]

func min : 
  [[[0 1 2 3]]]
```

**代码 2 :**

## 计算机编程语言

```py
# Python Program illustrating
# apply_over_axis() in NumPy

import numpy as geek

# Using a 2D array
geek_array = geek.arange(16).reshape(4, 4)
print("geek array  :\n", geek_array)

"""
    ->[[ 0  1  2  3]    min : 0     max : 3    sum =  0 + 1 + 2 + 3
    -> [ 4  5  6  7]    min : 4     max : 7    sum =  4 + 5 + 6 + 7
    -> [ 8  9 10 11]    min : 8     max : 11   sum =  8 + 9 + 10 + 11
    -> [12 13 14 15]]   min : 12    max : 15   sum =  12 + 13 + 14 + 15

"""

# Applying pre-defined min function over the axis of 2D array
print("\nApplying func max : \n ", geek.apply_over_axes(geek.max, geek_array, [1, -1]))

# Applying pre-defined min function over the axis of 2D array
print("\nApplying func min : \n ", geek.apply_over_axes(geek.min, geek_array, [1, -1]))

# Applying pre-defined sum function over the axis of 2D array
print("\nApplying func sum : \n ", geek.apply_over_axes(geek.sum, geek_array, [1, -1]))
```

**输出:**

```py
geek array  :
 [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]
 [12 13 14 15]]

Applying func max : 
  [[ 3]
 [ 7]
 [11]
 [15]]

Applying func min : 
  [[ 0]
 [ 4]
 [ 8]
 [12]]

Applying func sum : 
  [[ 6]
 [22]
 [38]
 [54]]
```

代码 3:不使用 numpy.apply_over_axis()等效于代码 2

## 计算机编程语言

```py
# Python Program illustrating
# equivalent to apply_over_axis()

import numpy as geek

# Using a 3D array
geek_array = geek.arange(16).reshape(2, 2, 4)
print("geek array  :\n", geek_array)

# returning sum of all elements as per the axis
print("func : \n", geek.sum(geek_array, axis=(1, 0, 2), keepdims = True))
```

**输出:**

```py
geek array  :
 [[[ 0  1  2  3]
  [ 4  5  6  7]]

 [[ 8  9 10 11]
  [12 13 14 15]]]
func : 
 [[[120]]]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . apply _ over _ axes . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.apply_over_axes.html)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。

本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。