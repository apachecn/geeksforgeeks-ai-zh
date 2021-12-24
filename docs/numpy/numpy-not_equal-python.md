# Python 中的 numpy.not_equal()

> 原文:[https://www.geeksforgeeks.org/numpy-not_equal-python/](https://www.geeksforgeeks.org/numpy-not_equal-python/)

**numpy.not_equal()** 检查两个元素是否相等。
**语法:**

```
numpy.not_equal(x1, x2[, out])

```

**参数:**

```
x1, x2 : [array_like]Input Array whose elements we want to check
out    : [ndarray, optional]Output array that returns True/False.
    A placeholder the same shape as x1 to store the result.

```

**返回:**

```
Boolean array 

```

**代码 1 :**

```
# Python Program illustrating
# numpy.not_equal() method

import numpy as geek 

a  = geek.not_equal([1., 2.], [1., 3.])
print("Not equal : \n", a, "\n")

b = geek.not_equal([1, 2], [[1, 3],[1, 4]])
print("Not equal : \n", b, "\n")
```

**输出:**

```
Not equal : 
 [False  True] 

Not equal : 
 [[False  True]
 [False  True]] 

```

**代码 2 :**

```
# Python Program illustrating
# numpy.not_equal() method

import numpy as geek 

# Here we will compare Complex values with int
a = geek.array([0 + 1j, 2])
b = geek.array([1,2])

d  = geek.not_equal(a, b)
print("Comparing complex with int using .not_equal() : ", d)
```

**输出:**

```
Comparing complex with int using .not_equal() :  [ True False]
```

**代码 3 :**

```
# Python Program illustrating
# numpy.not_equal() method

import numpy as geek 

# Here we will compare Float with int values
a = geek.array([1.1, 1])
b = geek.array([1, 2])

d  = geek.not_equal(a, b)
print("\nComparing float with int using .not_equal() : ", d)
```

**输出:**

```
 Comparing float with int using .not_equal() :  [ True  True]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . not _ equal . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.not_equal.html)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作的
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。