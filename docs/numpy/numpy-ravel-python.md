# Python 中的 numpy.ravel()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ravel-python/

**numpy.ravel()** 函数返回连续的扁平数组(包含所有输入数组元素且类型相同的 1D 数组)。只有在需要时才制作副本。
**语法:**

```py
numpy.ravel(array, order = 'C')
```

**参数:**

```py
array : [array_like]Input array. 
order : [C-contiguous, F-contiguous, A-contiguous; optional]         
         C-contiguous order in memory(last index varies the fastest)
         C order means that operating row-rise on the array will be slightly quicker
         FORTRAN-contiguous order in memory (first index varies the fastest).
         F order means that column-wise operations will be faster. 
         ‘A’ means to read / write the elements in Fortran-like index order if,
         array is Fortran contiguous in memory, C-like order otherwise
```

**返回:**

```py
Flattened array having same type as the Input array and and order as per choice. 
```

**代码 1:显示 array.ravel 相当于重塑(-1，order=order)**

## 计算机编程语言

```py
# Python Program illustrating
# numpy.ravel() method

import numpy as geek

array = geek.arrange(15).reshape(3, 5)
print("Original array : \n", array)

# Output comes like [ 0  1  2 ..., 12 13 14]
# as it is a long output, so it is the way of
# showing output in Python
print("\nravel() : ", array.ravel())

# This shows array.ravel is equivalent to reshape(-1, order=order).
print("\nnumpy.ravel() == numpy.reshape(-1)")
print("Reshaping array : ", array.reshape(-1))
```

**输出:**

```py
Original array : 
 [[ 0  1  2  3  4]
 [ 5  6  7  8  9]
 [10 11 12 13 14]]

ravel() :  [ 0  1  2 ..., 12 13 14]

numpy.ravel() == numpy.reshape(-1)
Reshaping array :  [ 0  1  2 ..., 12 13 14]
```

**代码 2:显示排序操作**

## 计算机编程语言

```py
# Python Program illustrating
# numpy.ravel() method

import numpy as geek

array = geek.arrange(15).reshape(3, 5)
print("Original array : \n", array)

# Output comes like [ 0  1  2 ..., 12 13 14]
# as it is a long output, so it is the way of
# showing output in Python

# About :
print("\nAbout numpy.ravel() : ", array.ravel)

print("\nnumpy.ravel() : ", array.ravel())

# Maintaining both 'A' and 'F' order
print("\nMaintains A Order : ", array.ravel(order = 'A'))

# K-order preserving the ordering
# 'K' means that is neither 'A' nor 'F'
array2 = geek.arrange(12).reshape(2,3,2).swapaxes(1,2)
print("\narray2 \n", array2)
print("\nMaintains A Order : ", array2.ravel(order = 'K'))
```

**输出:**

```py
Original array : 
 [[ 0  1  2  3  4]
 [ 5  6  7  8  9]
 [10 11 12 13 14]]

About numpy.ravel() :  

numpy.ravel() :  [ 0  1  2 ..., 12 13 14]

Maintains A Order :  [ 0  1  2 ..., 12 13 14]

array2 
 [[[ 0  2  4]
  [ 1  3  5]]

 [[ 6  8 10]
  [ 7  9 11]]]

Maintains A Order :  [ 0  1  2 ...,  9 10 11]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . ravel . html # numpy . ravel](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.ravel.html#numpy.ravel)
**注意:**
这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作方式
。
本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。