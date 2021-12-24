# Python 中的 numpy.tile()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-tile-python/

**numpy.tile()** 函数通过重复数组–“arr”来构造一个新的数组，arr 是我们每次重复的次数。生成的数组将具有最大尺寸(arr.ndim，repeats)，其中 repeats 是重复的长度。
如果重复一次，重复次数将被提升为 1 次。
如果 arr.ndim <重复，则通过预先待定的新轴将代表提升为 arr.ndim。
**语法:**

```py
numpy.tile(arr, repetitions)
```

**参数:**

```py
array       : [array_like]Input array. 
repetitions : No. of repetitions of arr along each axis. 

```

**返回:**

```py
An array with repetitions of array - arr as per d, number of times we want to repeat arr  

```

**代码 1 :**

```py
# Python Program illustrating
# numpy.tile()

import numpy as geek

#Working on 1D
arr = geek.arange(5)
print("arr : \n", arr)

repetitions = 2
print("Repeating arr 2 times : \n", geek.tile(arr, repetitions))

repetitions = 3
print("\nRepeating arr 3 times : \n", geek.tile(arr, repetitions))
# [0 1 2 ..., 2 3 4] means [0 1 2 3 4 0 1 2 3 4 0 1 2 3 4]
# since it was long output, so it uses [ ... ]
```

**输出:**

```py
arr : 
 [0 1 2 3 4]
Repeating arr 2 times : 
 [0 1 2 3 4 0 1 2 3 4]

Repeating arr 3 times : 
 [0 1 2 ..., 2 3 4]

```

**代码 2 :**

```py
# Python Program illustrating
# numpy.tile()

import numpy as geek

arr = geek.arange(3)
print("arr : \n", arr)

a = 2  
b = 2  
repetitions = (a, b)
print("\nRepeating arr : \n", geek.tile(arr, repetitions))
print("arr Shape : \n", geek.tile(arr, repetitions).shape)

a = 3  
b = 2   
repetitions = (a, b)
print("\nRepeating arr : \n", geek.tile(arr, repetitions))
print("arr Shape : \n", geek.tile(arr, repetitions).shape)

a = 2
b = 3  
repetitions = (a, b)
print("\nRepeating arr : \n", geek.tile(arr, repetitions))
print("arr Shape : \n", geek.tile(arr, repetitions).shape)
```

**输出:**

```py
arr : 
 [0 1 2]

Repeating arr : 
 [[0 1 2 0 1 2]
 [0 1 2 0 1 2]]
arr Shape : 
 (2, 6)

Repeating arr : 
 [[0 1 2 0 1 2]
 [0 1 2 0 1 2]
 [0 1 2 0 1 2]]
arr Shape : 
 (3, 6)

Repeating arr : 
 [[0 1 2 ..., 0 1 2]
 [0 1 2 ..., 0 1 2]]
arr Shape : 
 (2, 9)

```

**代码 3:(重复== arr.ndim) == 0**

```py
# Python Program illustrating
# numpy.tile()

import numpy as geek

arr = geek.arange(4).reshape(2, 2)
print("arr : \n", arr)

a = 2  
b = 1  
repetitions = (a, b)
print("\nRepeating arr : \n", geek.tile(arr, repetitions))
print("arr Shape : \n", geek.tile(arr, repetitions).shape)

a = 3  
b = 2   
repetitions = (a, b)
print("\nRepeating arr : \n", geek.tile(arr, repetitions))
print("arr Shape : \n", geek.tile(arr, repetitions).shape)

a = 2
b = 3  
repetitions = (a, b)
print("\nRepeating arr : \n", geek.tile(arr, repetitions))
print("arr Shape : \n", geek.tile(arr, repetitions).shape)
```

**输出:**

```py
arr : 
 [[0 1]
 [2 3]]

Repeating arr : 
 [[0 1]
 [2 3]
 [0 1]
 [2 3]]
arr Shape : 
 (4, 2)

Repeating arr : 
 [[0 1 0 1]
 [2 3 2 3]
 [0 1 0 1]
 [2 3 2 3]
 [0 1 0 1]
 [2 3 2 3]]
arr Shape : 
 (6, 4)

Repeating arr : 
 [[0 1 0 1 0 1]
 [2 3 2 3 2 3]
 [0 1 0 1 0 1]
 [2 3 2 3 2 3]]
arr Shape : 
 (4, 6)

```

**参考文献:**
[https://docs . scipy . org/doc/numpy/reference/generated/numpy . tile . html](https://docs.scipy.org/doc/numpy/reference/generated/numpy.tile.html)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作的
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。