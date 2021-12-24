# NumPy Python 中的基本切片和高级索引

> 原文:[https://www.geeksforgeeks.org/indexing-in-numpy/](https://www.geeksforgeeks.org/indexing-in-numpy/)

**先决条件:**Python 中的 [Numpy 简介](https://write.geeksforgeeks.org/introduction-to-numpy-set-1-all-changes-made/)
NumPy 或 Numeric Python 是一个在齐次 n 维数组上进行计算的包。在 numpy 中，维度称为轴。

**我们为什么需要 NumPy？**

一个问题出现了，既然 python 列表已经存在，为什么我们还需要 NumPy。答案是我们不能直接对两个列表的所有元素执行操作。例如，我们不能直接将两个列表相乘，我们必须按元素进行。这就是 NumPy 发挥作用的地方。

## 计算机编程语言

```
# Python program to demonstrate a need of NumPy

list1 = [1, 2, 3, 4 ,5, 6]
list2 = [10, 9, 8, 7, 6, 5]

# Multiplying both lists directly would give an error.
print(list1*list2)
```

**输出:**

```
TypeError: can't multiply sequence by non-int of type 'list'
```

这可以很容易地用 NumPy 阵列来完成。

另一个例子，

## 计算机编程语言

```
# Python program to demonstrate the use of NumPy arrays
import numpy as np

list1 = [1, 2, 3, 4, 5, 6]
list2 = [10, 9, 8, 7, 6, 5]

# Convert list1 into a NumPy array
a1 = np.array(list1)

# Convert list2 into a NumPy array
a2 = np.array(list2)

print(a1*a2)
```

**输出:**

```
array([10, 18, 24, 28, 30, 30])
```

本文将帮助您详细了解 NumPy 中的索引。python 的 Numpy 包具有以不同方式索引的强大功能。

**使用索引数组进行索引**

通过使用数组作为索引，可以在 numpy 中进行索引。在切片的情况下，返回数组的视图或浅层副本，但在索引数组中，返回原始数组的副本。Numpy 数组可以用除元组之外的其他数组或任何其他序列进行索引。最后一个元素的索引是-1 秒，最后一个是-2，依此类推。

## 计算机编程语言

```
# Python program to demonstrate
# the use of index arrays.
import numpy as np

# Create a sequence of integers from 10 to 1 with a step of -2
a = np.arrange(10, 1, -2)
print("\n A sequential array with a negative step: \n",a)

# Indexes are specified inside the np.array method.
newarr = a[np.array([3, 1, 2 ])]
print("\n Elements at these indices are:\n",newarr)
```

**输出:**

```
A sequential array with a negative step:
[10  8  6  4  2]

Elements at these indices are:
[4 8 6]
```

另一个例子，

## 计算机编程语言

```
import numpy as np

# NumPy array with elements from 1 to 9
x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9])

# Index values can be negative.
arr = x[np.array([1, 3, -3])]
print("\n Elements are : \n",arr)
```

**输出:**

```
Elements are:
[2 4 7]
```

**索引类型**

有两种类型的索引:

**1。基本切片和索引:**考虑语法 x[obj]，其中 x 是数组，obj 是索引。切片对象是基本切片情况下的索引。当 obj 为:

1.  具有开始:停止:步骤形式的切片对象
2.  整数
3.  或者切片对象和整数的元组

基本切片生成的所有数组都是原始数组的视图。

## 计算机编程语言

```
# Python program for basic slicing.
import numpy as np

# Arrange elements from 0 to 19
a = np.arrange(20)
print("\n Array is:\n ",a)

# a[start:stop:step]
print("\n a[-8:17:1] = ",a[-8:17:1])

# The : operator means all elements till the end.
print("\n a[10:] = ",a[10:])
```

**输出:**

```
Array is:
[ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19]

a[-8:17:1]  =  [12 13 14 15 16]

a[10:] = [10 11 12 13 14 15 16 17 18 19] 
```

省略号也可以和基本切片一起使用。省略号(…)是组成与数组维数相同长度的选择元组所需的:对象数。

## 计算机编程语言

```
# Python program for indexing using basic slicing with ellipsis
import numpy as np

# A 3 dimensional array.
b = np.array([[[1, 2, 3],[4, 5, 6]],
            [[7, 8, 9],[10, 11, 12]]])

print(b[...,1]) #Equivalent to b[: ,: ,1 ]
```

**输出:**

```
[[ 2  5]
 [ 8 11]]
```

**2。高级索引:**当对象为:

*   整数或布尔类型的数组
*   或者具有至少一个序列对象的元组
*   是非元组序列对象

高级索引返回数据的副本，而不是视图。高级索引有整数和布尔两种类型。

**纯整数索引:**使用整数进行索引时。第一维度的每个元素与第二维度的元素配对。所以在这种情况下，元素的索引是(0，0)，(1，0)，(2，1)，并选择相应的元素。

## 计算机编程语言

```
# Python program showing advanced indexing
import numpy as np

a = np.array([[1 ,2 ],[3 ,4 ],[5 ,6 ]])
print(a[[0 ,1 ,2 ],[0 ,0 ,1]])
```

**输出:**

```
[1 3 6]
```

**布尔索引**
这个索引有一些布尔表达式作为索引。返回那些满足布尔表达式的元素。它用于过滤所需的元素值。

## 计算机编程语言

```
# You may wish to select numbers greater than 50
import numpy as np

a = np.array([10, 40, 80, 50, 100])
print(a[a>50])
```

**输出:**

```
[80 100]
```

## 计算机编程语言

```
# You may wish to square the multiples of 40
import numpy as np

a = np.array([10, 40, 80, 50, 100])
print(a[a%40==0]**2)
```

**输出:**

```
[1600 6400])
```

## 计算机编程语言

```
# You may wish to select those elements whose
# sum of row is a multiple of 10.
import numpy as np

b = np.array([[5, 5],[4, 5],[16, 4]])
sumrow = b.sum(-1)
print(b[sumrow%10==0])
```

**输出:**

```
array([[ 5, 5], [16, 4]])
```

**参考:**
SciPy.org
本文由 **Ayushi Asthana** 供稿。如果你喜欢 GeeksforGeeks 并想投稿，你也可以用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。