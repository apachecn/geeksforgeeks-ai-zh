# python 中的 numpy.isfinite()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-isfinite python/

**numpy . is inite()**函数逐元素测试它是否是有限的(不是无穷大也不是数字)，并将结果作为布尔数组返回。
**语法:**

```
numpy.isfinite(array [, out])
```

**参数:**

```
array : [array_like]Input array or object whose elements, 
        we need to test for infinity
out   : [ndarray, optional]Output array placed with result.
       Its type is preserved and it must be of the right 
       shape to hold the output.

```

**返回:**

```
boolean array containing the result

```

**代码 1 :**

```
# Python Program illustrating
# numpy.isfinite() method

import numpy as geek 

print("Finite : ", geek.isfinite(1), "\n")

print("Finite : ", geek.isfinite(0), "\n")

# not a number
print("Finite : ", geek.isfinite(geek.nan), "\n")

#  infinity
print("Finite : ", geek.isfinite(geek.inf), "\n")

print("Finite : ", geek.isfinite(geek.NINF), "\n")  
```

**输出:**

```
Finite :  True 

Finite :  True 

Finite :  False 

Finite :  False 

Finite :  False 

```

**代码 2 :**

```
# Python Program illustrating
# numpy.isfinite() method

import numpy as geek 

# Returns True/False value for each element 
b = geek.arange(20).reshape(5, 4)

print("\n",b)
print("\nIs Finite : \n", geek.isfinite(b))

b = [[1j], 
     [geek.inf]]
print("\nIs Finite : \n", geek.isfinite(b))
```

**输出:**

```
 [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]
 [12 13 14 15]
 [16 17 18 19]]

Is Finite : 
 [[ True  True  True  True]
 [ True  True  True  True]
 [ True  True  True  True]
 [ True  True  True  True]
 [ True  True  True  True]]

Is Finite : 
 [[ True]
 [False]]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . is inite . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.isfinite.html)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。