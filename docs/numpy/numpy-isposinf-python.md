# numpy.isposinf()在 Python

中的应用

> 哎哎哎::1230【https://www . geeksforgeeks . org/num py-isposinf-python/

**numpy . isposif()**函数逐元素测试它是否为正无穷大，并将结果作为布尔数组返回。

**语法:**

```py
numpy.isposinf(array, y = None)
```

**参数:**

```py
array : [array_like]Input array or object whose elements, we need to test for infinity.
y     : [array_like]A boolean array with the same shape and type as x to store the result.
```

**返回:**

```py
boolean array containing the result. For scalar input, the result is a new boolean with value
True if the input is positive or negative infinity; otherwise the value is False.
For array input, the result is a boolean array with the same shape as the input and the values
are True where the corresponding element of the input is positive or negative infinity; 
elsewhere the values are False.
```

**代码 1:**

## 计算机编程语言

```py
# Python Program illustrating
# numpy.isposinf() method

import numpy as geek

print("Positive : ", geek.isposinf(1), "\n")

print("Positive : ", geek.isposinf(0), "\n")

# not a number
print("Positive : ", geek.isposinf(geek.nan), "\n")

#  infinity
print("Positive : ", geek.isposinf(geek.inf), "\n")

print("Positive : ", geek.isposinf(geek.NINF), "\n")

x = geek.array([-geek.inf, 0., geek.inf])
y = geek.array([2, 2, 2])
print("Checking for positivity : ", geek.isposinf(x, y))
```

**输出:**

```py
Positive :  False 

Positive :  False 

Positive :  False 

Positive :  True 

Positive :  False 

Checking for positivity :  [0 0 1]
```

**代码 2 :**

## 计算机编程语言

```py
# Python Program illustrating
# numpy.isposinf() method

import numpy as geek

# Returns True/False value for each element
b = geek.arange(18).reshape(3, 6)

print("\n",b)
print("\nIs Positive Infinity : \n", geek.isposinf(b))

# geek.inf means Infinity
# geek.NINF means negative infinity
b = [[geek.inf],
     [geek.NINF]]
print("\nIs Positive Infinity : \n", geek.isposinf(b))
```

**输出:**

```py
 [[ 0  1  2  3  4  5]
 [ 6  7  8  9 10 11]
 [12 13 14 15 16 17]]

Is Positive Infinity : 
 [[False False False False False False]
 [False False False False False False]
 [False False False False False False]]

Is Positive Infinity : 
 [[ True]
 [False]]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . isposif . html # numpy . isposif](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.isposinf.html#numpy.isposinf)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。

本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。