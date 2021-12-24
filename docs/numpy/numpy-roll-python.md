# python 中的 numpy.roll()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py roll python/

**numpy.roll()** 函数沿着指定的轴滚动数组元素。基本上发生的是输入数组的元素被移动。如果一个元素首先被滚动到最后一个位置，它将被回滚到第一个位置。

**语法:**

```py
numpy.roll(array, shift, axis = None)
```

**参数:**

```py
array : [array_like][array_like]Input array, whose elements we want to roll
shift : [int or int_tuple]No. of times we need to shift array elements.
        If a tuple, then axis must be a tuple of the same size, and each of the given 
        axes is shifted
        by the corresponding number. 
        If an int while axis is a tuple of ints, then the same value is used for all given axes.
axis  :  [array_like]Plane, along which we wish to roll array or shift it's elements.
```

**返回:**

```py
Output rolled array, with the same shape as a.
```

## 计算机编程语言

```py
# Python Program illustrating
# numpy.roll() method

import numpy as geek

array = geek.arange(12).reshape(3, 4)
print("Original array : \n", array)

# Rolling array; Shifting one place
print("\nRolling with 1 shift : \n", geek.roll(array, 1))

# Rolling array; Shifting five places
print("\nRolling with 5 shift : \n", geek.roll(array, 5))

# Rolling array; Shifting five places with 0th axis
print("\nRolling with 2 shift with 0 axis : \n", geek.roll(array, 2, axis = 0))
```

**输出:**

```py
Original array : 
 [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]

Rolling with 1 shift : 
 [[11  0  1  2]
 [ 3  4  5  6]
 [ 7  8  9 10]]

Rolling with 5 shift : 
 [[ 7  8  9 10]
 [11  0  1  2]
 [ 3  4  5  6]]

Rolling with 2 shift with 0 axis : 
 [[ 4  5  6  7]
 [ 8  9 10 11]
 [ 0  1  2  3]]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . roll . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.roll.html)
**注意:**
这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作。
本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。