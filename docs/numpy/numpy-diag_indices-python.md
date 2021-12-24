# numpy.diag_indices()用 Python

表示

> 哎哎哎::1230【https://www . geeksforgeeks . org/num py-diag _ indices-python/

**numpy . diag _ indexes()**函数返回索引，以便访问最小维数= 2 的数组的主对角线元素。以元组的形式返回索引。
访问一个数组的主对角线。

```
Syntax: numpy.diag_indices(n, n_dim = 2)
```

**参数:**

```
n : size of array, for which indices of diag elements are required along each dimension
n_dim  : [int, optional]number of dimensions. 
```

**返回:**

```
Indices(as tuples) to access diagonal elements.
```

**代码 1 :**

## 蟒蛇 3

```
# Python Program illustrating
# working of diag_indices()

import numpy as geek

# Creates a 5 X 5 array and returns indices of
# main diagonal elements
d = geek.diag_indices(5)
print("Indices of diagonal elements as tuple : ")
print(d, "\n")

array = geek.arange(16).reshape(4,4)
print("Initial array : \n", array)

# Here we can manipulate diagonal elements
# by accessing the diagonal elements
d = geek.diag_indices(4)
array[d] = 25
print("\n New array : \n", array)
```

**输出:**

```
Indices of diagonal elements as tuple : 
(array([0, 1, 2, 3, 4]), array([0, 1, 2, 3, 4])) 

Initial array : 
 [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]
 [12 13 14 15]]

 New array : 
 [[25  1  2  3]
 [ 4 25  6  7]
 [ 8  9 25 11]
 [12 13 14 25]]
```

**代码 2:操控 2D 阵**

## 计算机编程语言

```
# Python Program illustrating
# working of diag_indices()

import numpy as geek

# Manipulating a 2D array
d = geek.diag_indices(3, 2)

array = geek.arange(12).reshape(4, 3)

array[d] = 111
print("Manipulated array : \n", array)
```

**输出:**

```
Manipulated array : 
 [[111   1   2]
 [  3 111   5]
 [  6   7 111]
 [  9  10  11]]
```

**代码 3:操纵 3D 阵列**

## 计算机编程语言

```
# Python Program illustrating
# working of diag_indices()

import numpy as geek

# Setting diagonal indices
d = geek.diag_indices(1, 2)
print("Diag indices : \n", d)

# Creating a 3D array with all ones
array = geek.ones((2, 2, 2), dtype=geek.int)
print("Initial array : \n", array)

# Manipulating a 3D array
array[d] = 0
print("New array : \n", array)
```

**输出:**

```
Diag indices : 
 (array([0]), array([0]))
Initial array : 
 [[[1 1]
  [1 1]]

 [[1 1]
  [1 1]]]
New array : 
 [[[0 0]
  [1 1]]

 [[1 1]
  [1 1]]]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . diag _ indexes . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.diag_indices.html)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。

本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。