# Python 中的 numpy.ones _ like()

> 原文:[https://www.geeksforgeeks.org/numpy-ones_like-python/](https://www.geeksforgeeks.org/numpy-ones_like-python/)

**numpy.one_like()** 函数返回一个给定形状和类型的数组作为给定数组，带 1。

```py
Syntax: numpy.ones_like(array, dtype = None, order = 'K', subok = True)
```

**参数:**

```py
array : array_like input
subok  : [optional, boolean]If true, then newly created array will be sub-class of array; 
                 otherwise, a base-class array
order  : C_contiguous or F_contiguous
         C-contiguous order in memory(last index varies the fastest)
         C order means that operating row-wise on the array will be slightly quicker
         FORTRAN-contiguous order in memory (first index varies the fastest).
         F order means that column-wise operations will be faster. 
dtype  : [optional, float(byDefault)] Data type of returned array.  

```

**返回:**

```py
ndarray of ones having given shape, order and datatype.
```

```py
# Python Programming illustrating
# numpy.ones_like method

import numpy as geek

array = geek.arange(10).reshape(5, 2)
print("Original array : \n", array)

b = geek.ones_like(array, float)
print("\nMatrix b : \n", b)

array = geek.arange(8)
c = geek.ones_like(array)
print("\nMatrix c : \n", c)
```

**输出:**

```py
Original array : 
 [[0 1]
 [2 3]
 [4 5]
 [6 7]
 [8 9]]

Matrix b : 
 [[ 1\.  1.]
 [ 1\.  1.]
 [ 1\.  1.]
 [ 1\.  1.]
 [ 1\.  1.]]

Matrix c : 
 [1 1 1 1 1 1 1 1]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . ones _ like . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.ones_like.html)
**注意:**
同样，这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作

本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。