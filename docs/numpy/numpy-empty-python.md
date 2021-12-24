# Python 中的 numpy.empty()

> 原文:[https://www.geeksforgeeks.org/numpy-empty-python/](https://www.geeksforgeeks.org/numpy-empty-python/)

**numpy.empty(shape，dtype = float，order = 'C') :** 返回给定形状和类型的新数组，带有随机值。
T3】参数:

```py
-> shape : Number of rows
-> order : C_contiguous or F_contiguous
-> dtype : [optional, float(by Default)] Data type of returned array.  

```

```py
# Python Programming illustrating
# numpy.empty method

import numpy as geek

b = geek.empty(2, dtype = int)
print("Matrix b : \n", b)

a = geek.empty([2, 2], dtype = int)
print("\nMatrix a : \n", a)

c = geek.empty([3, 3])
print("\nMatrix c : \n", c)
```

**输出:**

```py
Matrix b : 
 [         0 1079574528]

Matrix a : 
 [[0 0]
 [0 0]]

Matrix a : 
 [[ 0\.  0\.  0.]
 [ 0\.  0\.  0.]
 [ 0\.  0\.  0.]]
```

**注意:**与零不同，空不会将数组值设置为零，因此可能会稍微快一些。
此外，这些代码不会在在线身份证上运行。请在您的系统上运行它们来探索工作

本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。