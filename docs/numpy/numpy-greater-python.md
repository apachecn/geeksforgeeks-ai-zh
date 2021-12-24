# Python 中的 numpy.greater()

> 原文:[https://www.geeksforgeeks.org/numpy-greater-python/](https://www.geeksforgeeks.org/numpy-greater-python/)

**numpy.greater()** 检查 x1 是否大于 x2。
**语法:**

```py
numpy.greater(x1, x2[, out]) 

```

**参数:**

```py
x1, x2 : [array_like]Input arrays. If x1.shape != x2.shape, they must be 
             broadcastable to a common shape 
out    : [ndarray, boolean]Array of bools, or a single bool if x1 and x2 are scalars.

```

**返回:**

```py
Boolean array indicating results, whether x1 is greater than x2 or not.

```

**代码 1 :**

```py
# Python Program illustrating
# numpy.greater() method

import numpy as geek 

a  = geek.greater([8., 2.], [5., 3.])
print("Not equal : \n", a, "\n")

b = geek.greater([2, 2], [[1, 3],[1, 4]])
print("Not equal : \n", b, "\n")

a = geek.array([4,2])
b = geek.array([6,2])

print("Is a greater than b : ", a > b)
```

**输出:**

```py
Not equal : 
 [ True False] 

Not equal : 
 [[ True False]
 [ True False]] 

Is a greater than b :  [False False]

```

**代码 2 :**

```py
# Python Program illustrating
# numpy.greater() method

import numpy as geek 

# Here we will compare Float with int values
a = geek.array([1.1, 1])
b = geek.array([1, 2])

# indicating 1.1 is greater than 1
print("Comparing float with int : ", a < b)

# indicating 1.1 is greater than 1
d  = geek.greater(a, b)
print("\n Comparing float with int using  .greater() : ", d)
```

**输出:**

```py
Comparing float with int :  [False  True]

 Comparing float with int using  .greater() :  [ True False]

```

**代码 3 :**

```py
# Python Program illustrating
# numpy.greater() method

import numpy as geek 

# Here we will compare Complex values with int 
a = geek.array([1j,2])
b = geek.array([1,2])

# indicating 1j is greater than 1
print("Comparing complex with int : ", a < b)

# indicating 1j is greater than 1
d  = geek.greater(a, b)
print("\nComparing complex with int using .greater() : ", d)
```

**输出:**

```py
Comparing complex with int :  [ True False]

Comparing complex with int using .greater() :  [False False]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . greater . html # numpy . greater](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.greater.html#numpy.greater)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作的
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。