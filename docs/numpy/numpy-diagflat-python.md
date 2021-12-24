# python 中的 numpy.diagflat()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-diag flat-python/

**numpy.diagflat (a，k = 0):** 创建一个二维数组，将 array_like 输入作为新输出数组的对角线。

**参数:**

```py
a : array_like input data with diagonal  elements
strong>k : [int, optional, 0 by default]
          Diagonal we require; k>0 means diagonal  above main diagonal  or vice versa.
```

**返回:**

```py
array with the array_like input as a diagonal to the new output array.
```

## 计算机编程语言

```py
# Python Program illustrating
# numpy.diagflat method

import numpy as geek

print("diagflat use on main diagonal : \n", geek.diagflat([1, 7]), "\n")

print("diagflat use on main diagonal : \n", geek.diagflat([1, 7, 6]), "\n")

# Diagonal above main diagonal
print("diagflat above main diagonal : \n", geek.diagflat([1, 7, 6], 1), "\n")
```

**输出:**

```py
diagflat use on main diagonal  : 
 [[1 0]
 [0 7]] 

diagflat use on main diagonal  : 
 [[1 0 0]
 [0 7 0]
 [0 0 6]] 

diagflat above main diagonal  : 
 [[0 1 0 0]
 [0 0 7 0]
 [0 0 0 6]
 [0 0 0 0]] 
```

**注意:**
这些 NumPy-Python 程序不会在 onlineID 上运行，所以在你的系统上运行它们来探索它们。

本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。