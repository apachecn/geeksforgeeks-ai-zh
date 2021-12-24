# Python 中的 numpy.less_equal()

> 原文:[https://www.geeksforgeeks.org/numpy-less_equal-python/](https://www.geeksforgeeks.org/numpy-less_equal-python/)

**numpy.less_equal()** 功能检查 x1 是否为< = x2。

**语法:**

```
numpy.less_equal(x1, x2[, out])
```

**参数:**

```
x1, x2 : [array_like]Input arrays. If x1.shape != x2.shape, they must be 
             broadcastable to a common shape 
out    : [ndarray, boolean]Array of bools, or a single bool if x1 and x2 are scalars.

```

**返回:**

```
Boolean array indicating results, whether x1 is lesser than x2 or not.

```

**代码 1 :**

```
# Python Program illustrating
# numpy.less_equal() method

import numpy as geek 

a  = geek.less_equal([8., 2.], [5., 3.])
print("less_equal() : \n", a, "\n")

b = geek.less_equal([2, 2], [[1, 3],[1, 4]])
print("less_equal() : \n", b, "\n")

a = geek.array([4,3])
b = geek.array([6,2])

print("Is a less_equal than b : ", a <= b)
```

**输出:**

```
less_equal() : 
 [False  True] 

less_equal() : 
 [[False  True]
 [False  True]] 

Is a less_equaler than b :  [ True False]

```

**代码 2 :**

```
# Python Program illustrating
# numpy.less_equal() method

import numpy as geek 

# Here we will compare Complex values with the 
a = geek.array([100j,7])
b = geek.array([1,2])

print("Comparing complex with int : ", a <= b)

d  = geek.less_equal(a, b)
print("\n Comparing complex with int  .less_equal() : ", d)
```

**输出:**

```
Comparing complex with int :  [ True False]

 Comparing complex with int  .less_equal() :  [ True False]

```

**代码 3 :**

```
# Python Program illustrating
# numpy.less_equal() method

import numpy as geek 

# Here we will compare Float with int values
a = geek.array([1.1, 1])
b = geek.array([1, 2])

print("Comparing float with int : ", a <= b)

d  = geek.less_equal(a, b)
print("\n Comparing float with int using  .less_equal() : ", d)
```

**输出:**

```
Comparing float with int :  [False  True]

 Comparing float with int using  .less_equal() :  [False  True]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . less . html # numpy . less](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.less.html#numpy.less)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。

本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。