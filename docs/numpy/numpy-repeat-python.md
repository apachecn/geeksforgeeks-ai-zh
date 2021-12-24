# Python 中的 numpy.repeat()

> 原文:[https://www.geeksforgeeks.org/numpy-repeat-python/](https://www.geeksforgeeks.org/numpy-repeat-python/)

**numpy.repeat()** 函数重复数组的元素–arr。
**语法:**

```py
numpy.repeat(arr, repetitions, axis = None)
```

**参数:**

```py
array       : [array_like]Input array. 
repetitions : No. of repetitions of each array elements along the given axis.
axis        : Axis along which we want to repeat values. By default, it returns 
           a flat output array.

```

**返回:**

```py
An array with repetitions of array - arr elements as per repetitions, number of times 
we want to repeat arr  

```

**代码 1 :**

```py
# Python Program illustrating
# numpy.repeat()

import numpy as geek

#Working on 1D
arr = geek.arange(5)
print("arr : \n", arr)

repetitions = 2
a = geek.repeat(arr, repetitions)
print("\nRepeating arr 2 times : \n", a)
print("Shape : ", a.shape)

repetitions = 3
a = geek.repeat(arr, repetitions)
print("\nRepeating arr 3 times : \n", a)
# [0 0 0 ..., 4 4 4] means [0 0 0 1 1 1 2 2 2 3 3 3 4 4 4]
# since it was long output, so it uses [ ... ]
print("Shape : ", a.shape)
```

**输出:**

```py
arr : 
 [0 1 2 3 4]

Repeating arr 2 times : 
 [0 0 1 1 2 2 3 3 4 4]
Shape :  (10,)

Repeating arr 3 times : 
 [0 0 0 ..., 4 4 4]
Shape :  (15,)

```

**代码 2 :**

```py
# Python Program illustrating
# numpy.repeat()

import numpy as geek

arr = geek.arange(6).reshape(2, 3)
print("arr : \n", arr)

repetitions = 2
print("\nRepeating arr : \n", geek.repeat(arr, repetitions, 1))
print("arr Shape : \n", geek.repeat(arr, repetitions).shape)

repetitions = 2
print("\nRepeating arr : \n", geek.repeat(arr, repetitions, 0))
print("arr Shape : \n", geek.repeat(arr, repetitions).shape)

repetitions = 3
print("\nRepeating arr : \n", geek.repeat(arr, repetitions, 1))
print("arr Shape : \n", geek.repeat(arr, repetitions).shape)
```

**输出:**

```py
arr : 
 [[0 1 2]
 [3 4 5]]

Repeating arr : 
 [[0 0 1 1 2 2]
 [3 3 4 4 5 5]]
arr Shape : 
 (12,)

Repeating arr : 
 [[0 1 2]
 [0 1 2]
 [3 4 5]
 [3 4 5]]
arr Shape : 
 (12,)

Repeating arr : 
 [[0 0 0 ..., 2 2 2]
 [3 3 3 ..., 5 5 5]]
arr Shape : 
 (18,)

```

**参考文献:**
[https://docs . scipy . org/doc/numpy/reference/generated/numpy . repeat . html](https://docs.scipy.org/doc/numpy/reference/generated/numpy.repeat.html)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作的
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。