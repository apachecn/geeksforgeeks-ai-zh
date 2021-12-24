# numpy.isinf()用 Python

表示

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-isinf-python/

**numpy.isinf()** 函数按元素测试是+ve 还是-ve 无穷大，并以布尔数组的形式返回结果。

```
Syntax: numpy.isinf(array [, out])
```

**参数:**

```
array : [array_like]Input array or object whose 
         elements, we need to test for  infinity
out   : [ndarray, optional]Output array placed 
        with result. Its type is preserved and
        it  must be of the right shape to hold 
         the output.
```

**返回:**

```
boolean array containing the result. For scalar 
input, the result is a new boolean with value
True if the input is positive or negative infinity; 
otherwise the value is False. For array input, the 
result is a boolean array with the same shape as 
the input and the values are True where the 
corresponding element of the input is positive
or negative infinity; elsewhere the values are False.
```

**代码 1 :**

## 计算机编程语言

```
# Python Program illustrating
# numpy.isinf() method

import numpy as geek

print("Finite : ", geek.isinf(1), "\n")

print("Finite : ", geek.isinf(0), "\n")

# not a number
print("Finite : ", geek.isinf(geek.nan), "\n")

#  infinity
print("Finite : ", geek.isinf(geek.inf), "\n")

print("Finite : ", geek.isinf(geek.NINF), "\n")

x = geek.array([-geek.inf, 0., geek.inf])
y = geek.array([2, 2, 2])
print("Checking for infinity : ", geek.isinf(x, y))
```

**输出:**

```
Finite :  False 

Finite :  False 

Finite :  False 

Finite :  True 

Finite :  True 

Checking for infinity :  [1 0 1]
```

**代码 2 :**

## 计算机编程语言

```
# Python Program illustrating
# numpy.isinf() method

import numpy as geek

# Returns True/False value for each element
b = geek.arange(8).reshape(2, 4)

print("\n",b)
print("\nIs Infinity : \n", geek.isinf(b))

# geek.inf  : Positive Infinity
# geek.NINF : negative Infinity
b = [[geek.inf],
     [geek.NINF]]
print("\nIs Infinity : \n", geek.isinf(b))
```

**输出:**

```
 [[0 1 2 3]
 [4 5 6 7]]

Is Infinity : 
 [[False False False False]
 [False False False False]]

Is Infinity : 
 [[ True]
 [ True]]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . is if . html # numpy . is if](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.isinf.html#numpy.isinf)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。

本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。