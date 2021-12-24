# Python 中的 numpy.put()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-put-python/

**numpy.put()** 函数用 p_array 的给定值替换数组的特定元素。数组索引适用于扁平数组。

```
Syntax: numpy.put(array, indices, p_array, mode = 'raise')
```

**参数:**

```
array   : array_like, target array
indices : index of the values to be fetched
p_array : array_like, values to be placed in target array
mode    : [{‘raise’, ‘wrap’, ‘clip’}, optional] mentions how out-of-bound indices will behave
                  raise : [default]raise an error 
                  wrap  : wrap around
                  clip  : clip to the range

```

```
# Python Program explaining
# numpy.put()

import numpy as geek

a = geek.arange(5)
geek.put(a, [0, 2], [-44, -55])
print("After put : \n", a)
```

**输出:**

```
After put : 
[-44,   1, -55,   3,   4]

```

```
# Python Program explaining
# numpy.put()

import numpy as geek

a = geek.arange(5)
geek.put(a, 22, -5, mode='clip')
print("After put : \n", a)
```

**输出:**

```
array([ 0,  1,  2,  3, -5])
```

**代码来源:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . put . html # numpy . put](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.put.html#numpy.put)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作的
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。