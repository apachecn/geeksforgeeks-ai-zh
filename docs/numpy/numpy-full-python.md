# Python 中的 numpy.full()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-full-python/

**numpy.full(shape，fill_value，dtype = None，order = 'C') :** 返回一个新数组，其形状和类型与填充 fill_value 的给定数组相同。
T3】参数:

```
shape      : Number of rows
order      : C_contiguous or F_contiguous
dtype      : [optional, float(by Default)] Data type of returned array.  
fill_value : [bool, optional] Value to fill in the array.

```

**返回:**

```
ndarray

```

```
# Python Programming illustrating
# numpy.full method

import numpy as geek

a = geek.full([2, 2], 67, dtype = int)
print("\nMatrix a : \n", a)

c = geek.full([3, 3], 10.1)
print("\nMatrix c : \n", c)
```

**输出:**

```

Matrix a : 
 [[67 67]
 [67 67]]

Matrix c : 
 [[ 10.1  10.1  10.1]
 [ 10.1  10.1  10.1]
 [ 10.1  10.1  10.1]]

```

**参考文献:**
[https://docs . scipy . org/doc/NumPy/reference/generated/NumPy . full . html # NumPy . full](https://docs.scipy.org/doc/numpy/reference/generated/numpy.full.html#numpy.full)
**注意:**
这些 NumPy-Python 程序不会在 onlineID 上运行，所以在你的系统上运行它们来探索它们
。
本文由 <font color="green">**莫希特·古普塔 _OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。