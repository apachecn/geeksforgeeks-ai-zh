# Python 中的 numpy.matrix()

> 原文:[https://www.geeksforgeeks.org/numpy-matrix-python/](https://www.geeksforgeeks.org/numpy-matrix-python/)

这个类从一串数据或类似数组的对象中返回一个矩阵。获得的矩阵是一个专门的 2D 阵列。
**语法:**

```py
numpy.matrix(data, dtype = None) : 
```

**参数:**

```py
data  : data needs to be array-like or string 
dtype : Data type of returned array. 

```

**返回:**

```py
data interpreted as a matrix
```

```py
# Python Program illustrating
# numpy.matrix class

import numpy as geek

# string input
a = geek.matrix('1 2; 3 4')
print("Via string input : \n", a, "\n\n")

# array-like input
b = geek.matrix([[5, 6, 7], [4, 6]])
print("Via array-like input : \n", b)
```

**输出:**

```py
Via string input : 
 [[1 2]
 [3 4]] 

Via array-like input : 
 [[[5, 6, 7] [4, 6]]]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy/reference/generated/numpy . mat . html # numpy . mat](https://docs.scipy.org/doc/numpy/reference/generated/numpy.mat.html#numpy.mat)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作的
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。