# Python 中的 numpy.take()

> 原文:[https://www.geeksforgeeks.org/numpy-take-python/](https://www.geeksforgeeks.org/numpy-take-python/)

**numpy.take()** 函数返回数组中沿上述轴和索引的元素。

```
Syntax: numpy.take(array, indices, axis = None, out = None, mode ='raise')
```

**参数:**

```
array   : array_like, input array
indices : index of the values to be fetched
axis    : [int, optional] axis over which we need to fetch the elements; 
                  By Default[axis = None], flattened input is used
mode    : [{‘raise’, ‘wrap’, ‘clip’}, optional] mentions how out-of-bound indices will behave
                  raise : [default]raise an error 
                  wrap  : wrap around
                  clip  : clip to the range
out     : [ndarray, optional]to place result within array

```

**返回:**

```
ndarray; array has the same type
```

```
# Python Program illustrating
# numpy.take method

import numpy as geek

#array = geek.arange(10).reshape(2, 5)
array = [[5, 6, 2, 7, 1],
         [4, 9, 2, 9, 3]]
print("Original array : \n", array)

# indices = [0, 4]
print("\nTaking Indices\n", geek.take(array, [0, 4]))

# indices = [0, 4] with axis = 1
print("\nTaking Indices\n", geek.take(array, [0, 4], axis = 1))
```

**输出:**

```
Original array : 
 [[5, 6, 2, 7, 1], [4, 9, 2, 9, 3]]

Taking Indices
 [5 1]

Taking Indices
 [[5 1]
 [4 3]]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . take . html # numpy . take](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.take.html#numpy.take)
**注意:**
这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。