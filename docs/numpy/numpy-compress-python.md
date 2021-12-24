# Python 中的 numpy.compress()

> 原文:[https://www.geeksforgeeks.org/numpy-compress-python/](https://www.geeksforgeeks.org/numpy-compress-python/)

**numpy.compress()** 函数返回沿所述轴的数组的选定切片，该切片满足一个轴。

```py
Syntax: numpy.compress(condition, array, axis = None, out = None)
```

**参数:**

```py
condition : [array_like]Condition on the basis of which user extract elements. 
      Applying condition on input_array, if we print condition, it will return an arra
      filled with either True or False. Array elements are extracted from the Indices having 
      True value.
array     : Input array. User apply conditions on input_array elements
axis      : [optional, int]Indicating which slice to select. 
         By Default, work on flattened array[1-D]
out       : [optional, ndarray]Output_array with elements of input_array, 
               that satisfies condition

```

**返回:**

```py
Copy of array with elements of input_array,
that satisfies condition and along given axis

```

```py
# Python Program illustrating
# numpy.compress method

import numpy as geek

array = geek.arange(10).reshape(5, 2)
print("Original array : \n", array)

a = geek.compress([0, 1], array, axis=0)
print("\nSliced array : \n", a)

a = geek.compress([False, True], array, axis=0)
print("\nSliced array : \n", a)
```

**输出:**

```py
Original array : 
 [[0 1]
 [2 3]
 [4 5]
 [6 7]
 [8 9]]

Sliced array : 
 [[2 3]]

Sliced array : 
 [[2 3]]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . compress . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.compress.html)
**注:**
这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作。
。
本文由 <font color="green">**莫希特·古普塔 _OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。