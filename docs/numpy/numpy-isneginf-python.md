# numpy . isnegnf()在 Python

中

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-isnegnf-python/

**numpy.isneginf()** 函数逐元素测试是否为负无穷大，并将结果作为布尔数组返回。
**语法:**

```
numpy.isneginf(array, y = None)
```

**参数:**

```
array : [array_like]Input array or object whose elements, we need to test for infinity.
y     : [array_like]A boolean array with the same shape and type as x to store the result.
```

**返回:**

```
boolean array containing the result. For scalar input, the result is a new boolean with value
True if the input is positive or negative infinity; otherwise the value is False.
For array input, the result is a boolean array with the same shape as the input and the values
are True where the corresponding element of the input is positive or negative infinity; 
elsewhere the values are False.
```

**代码 1 :**

## 计算机编程语言

```
# Python Program illustrating
# numpy.isneginf() method

import numpy as geek

print("Negative : ", geek.isneginf(1), "\n")

print("Negative : ", geek.isneginf(0), "\n")

# not a number
print("Negative : ", geek.isneginf(geek.nan), "\n")

#  infinity
print("Negative : ", geek.isneginf(geek.inf), "\n")

print("Negative : ", geek.isneginf(geek.NINF), "\n")

x = geek.array([-geek.inf, 0., geek.inf])
y = geek.array([2, 2, 2])
print("Checking for negativity : ", geek.isneginf(x, y))
```

**输出:**

```
Negative :  False 

Negative :  False 

Negative :  False 

Negative :  False 

Negative :  True 

Checking for negativity :  [1 0 0]
```

**代码 2 :**

## 计算机编程语言

```
# Python Program illustrating
# numpy.isneginf() method

import numpy as geek

# Returns True/False value for each element
b = geek.arange(18).reshape(3, 6)

print("\n",b)
print("\nIs Negative Infinity : \n", geek.isneginf(b))

# geek.inf  : Positive Infinity
# geek.NINF : negative Infinity
b = [[geek.inf],
     [geek.NINF]]
print("\nIs Negative Infinity : \n", geek.isneginf(b))
```

**输出:**

```
 [[ 0  1  2  3  4  5]
 [ 6  7  8  9 10 11]
 [12 13 14 15 16 17]]

Is Negative Infinity : 
 [[False False False False False False]
 [False False False False False False]
 [False False False False False False]]

Is Negative Infinity : 
 [[False]
 [ True]]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . isneginf . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.isneginf.html)
**注:**
这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作。
。
本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。