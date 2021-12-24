# Python 中的 numpy.dot()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-dot-python/

numpy.dot(vector_a，vector_b，out = None)返回向量 a 和 b 的点积。它可以处理 2D 数组，但会将它们视为矩阵，并将执行矩阵乘法。对于 N 维，它是 a 的最后一个轴和 b 的倒数第二个轴的和积:

```
dot(a, b)[i,j,k,m] = sum(a[i,j,:] * b[k,:,m]) 

```

**参数**

1.  **vector _ a:**【array _ like】如果 a 是复数，其复共轭用于点积的计算。
2.  **vector _ b:**【array _ like】如果 b 是复数，则其复共轭用于点积的计算。
3.  **out :** 【数组，可选】输出参数必须是 C 连续的，其数据类型必须是将为点(a，b)返回的数据类型。

**返回:**

向量 a 和 b 的点积。如果向量 a 和向量 b 是 1D，则返回标量

**代码 1:**

## 计算机编程语言

```
# Python Program illustrating
# numpy.dot() method

import numpy as geek

# Scalars
product = geek.dot(5, 4)
print("Dot Product of scalar values  : ", product)

# 1D array
vector_a = 2 + 3j
vector_b = 4 + 5j

product = geek.dot(vector_a, vector_b)
print("Dot Product  : ", product)
```

**输出:**

```
Dot Product of scalar values  :  20
Dot Product  :  (-7+22j)
```

> 【Code1 是如何工作的？
> 
> vector_a = 2 + 3j
> 
> vector_b = 4 + 5j
> 
> 现在点积
> 
> = 2(4+5j)+3j(4–5j)
> 
> = 8+10j+12j–15
> 
> = -7 + 22j

**代码 2:**

## 计算机编程语言

```
# Python Program illustrating
# numpy.dot() method

import numpy as geek

# 1D array
vector_a = geek.array([[1, 4], [5, 6]])
vector_b = geek.array([[2, 4], [5, 2]])

product = geek.dot(vector_a, vector_b)
print("Dot Product  : \n", product)

product = geek.dot(vector_b, vector_a)
print("\nDot Product  : \n", product)

"""
Code 2 : as normal matrix multiplication
"""
```

**输出:**

```
Dot Product  : 
 [[22 12]
 [40 32]]

Dot Product  : 
 [[22 32]
 [15 32]]
```

**参考文献:**[https://numpy . org/doc/stable/reference/generated/numpy . dot . html](https://numpy.org/doc/stable/reference/generated/numpy.dot.html)

本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。