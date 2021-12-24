# num py . red 90()python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-red 90-python/

**numpy.rot90()** 方法在轴(0 或 1)指定的平面内将数组旋转 90 度。
**语法:**

```
numpy.rot90(array, k = 1, axes = (0, 1))
```

**参数:**

```
array : [array_like]i.e. array having two or more dimensions.
k     : [optional , int]No. of times we wish to rotate array by 90 degrees.
axes  : [array_like]Plane, along which we wish to rotate array.

```

**返回:**

```
rotated copy of array

```

```
# Python Program illustrating
# numpy.rot90() method

import numpy as geek

array = geek.arange(12).reshape(3, 4)
print("Original array : \n", array)

# Rotating array 4 times : Returns same original array
print("\nArray being rotated 4 times : \n", geek.rot90(array, 4))

# Rotating once
print("\nRotated array : \n", geek.rot90(array))

# Rotating twice
print("\nRotated array : \n", geek.rot90(array, 2))
```

**输出:**

```
Original array : 
 [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]

Array being rotated 4 times : 
 [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]

Rotated array : 
 [[ 3  7 11]
 [ 2  6 10]
 [ 1  5  9]
 [ 0  4  8]]

Rotated array : 
 [[11 10  9  8]
 [ 7  6  5  4]
 [ 3  2  1  0]]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . rot 90 . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.rot90.html)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作的
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。