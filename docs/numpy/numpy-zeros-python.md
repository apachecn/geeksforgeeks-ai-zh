# Python 中的 numpy.zeros()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-zero-python/

**numpy.zeros()** 函数返回一个给定形状和类型的新数组，带有零。
**语法:**

```py
numpy.zeros(shape, dtype = None, order = 'C')
```

**参数:**

```py
shape : integer or sequence of integers
order  : C_contiguous or F_contiguous
         C-contiguous order in memory(last index varies the fastest)
         C order means that operating row-rise on the array will be slightly quicker
         FORTRAN-contiguous order in memory (first index varies the fastest).
         F order means that column-wise operations will be faster. 
dtype : [optional, float(byDeafult)] Data type of returned array.  

```

**返回:**

```py
ndarray of zeros having given shape, order and datatype.
```

 **代码 1 :**

```py
# Python Program illustrating
# numpy.zeros method

import numpy as geek

b = geek.zeros(2, dtype = int)
print("Matrix b : \n", b)

a = geek.zeros([2, 2], dtype = int)
print("\nMatrix a : \n", a)

c = geek.zeros([3, 3])
print("\nMatrix c : \n", c)
```

**输出:**

```py
Matrix b : 
 [0 0]

Matrix a : 
 [[0 0]
 [0 0]]

Matrix c : 
 [[ 0\.  0\.  0.]
 [ 0\.  0\.  0.]
 [ 0\.  0\.  0.]]

```

 **代码 2:操纵数据类型**

```py
# Python Program illustrating
# numpy.zeros method

import numpy as geek

# manipulation with data-types
b = geek.zeros((2,), dtype=[('x', 'float'), ('y', 'int')])
print(b)
```

**输出:**

```py
[(0.0, 0) (0.0, 0)]

```

**Reference:**
[https://docs . scipy . org/doc/numpy-dev/Reference/generated/numpy . zeros . html # numpy . zeros](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.zeros.html#numpy.zeros)
**注意:** zeros 与零和空不同，不会将数组值分别设置为零或随机值。此外，这些代码不会在在线身份证上运行。请在您的系统上运行它们来探索工作。

本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。