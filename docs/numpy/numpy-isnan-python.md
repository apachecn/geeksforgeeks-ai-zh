# numpy.isnan()用 Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-isnan-python/

**numpy.isnan()** 函数逐元素测试它是否是 nan，并将结果作为布尔数组返回。
**语法:**

```py
numpy.isnan(array [, out])
```

**参数:**

```py
array : [array_like]Input array or object whose elements, we need to test for infinity
out   : [ndarray, optional]Output array placed with result.
      Its type is preserved and it must be of the right shape to hold the output.

```

**返回:**

```py
boolean array containing the result. For scalar input, the result is a new boolean with value
True if the input is positive or negative infinity; otherwise the value is False.
For array input, the result is a boolean array with the same shape as the input and the values
are True where the corresponding element of the input is positive or negative infinity; 
elsewhere the values are False.

```

**代码 1 :**

```py
# Python Program illustrating
# numpy.isnan() method

import numpy as geek 

print("Is NaN : ", geek.isnan(1), "\n")

print("Is NaN : ", geek.isnan(0), "\n")

# not a number
print("Is NaN : ", geek.isnan(geek.nan), "\n")

#  infinity
print("Is NaN : ", geek.isnan(geek.inf), "\n")

print("Is NaN : ", geek.isnan(geek.NINF), "\n") 

x = geek.array([-geek.inf, 0., geek.inf])
y = geek.array([2, 2, 2])
print("Checking for NaN : ", geek.isnan(x, y))

```

**输出:**

```py
Is NaN :  False 

Is NaN :  False 

Is NaN :  True 

Is NaN :  False 

Is NaN :  False 

Checking for NaN :  [0 0 0]

```

**代码 2 :**

```py
# Python Program illustrating
# numpy.isnan() method

import numpy as geek 

# Returns True/False value for each element 
b = geek.arange(20).reshape(5, 4)

print("\n",b)
print("\nIs NaN(Not a Number): \n", geek.isnan(b))

b = [[1j], 
     [geek.nan]]
print("\nIs NaN(Not a Number) : \n", geek.isnan(b))
```

**输出:**

```py
 [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]
 [12 13 14 15]
 [16 17 18 19]]

Is NaN(Not a Number): 
 [[False False False False]
 [False False False False]
 [False False False False]
 [False False False False]
 [False False False False]]

Is NaN(Not a Number) : 
 [[False]
 [ True]]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . isnan . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.isnan.html)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。