# 创建一个充满所有 1 的 Numpy 数组

> 原文:[https://www . geeksforgeeks . org/create-a-numpy-array-filled-all-one/](https://www.geeksforgeeks.org/create-a-numpy-array-filled-with-all-ones/)

在本文中，我们将学习如何在给定数组的形状和类型的情况下，创建一个全为 1 的 Numpy 数组。

我们可以使用 Numpy.ones()方法来完成这个任务。该方法采用三个参数，讨论如下–

```py
shape : integer or sequence of integers
order  : C_contiguous or F_contiguous
         C-contiguous order in memory(last index varies the fastest)
         C order means that operating row-rise on the array will be slightly quicker
         FORTRAN-contiguous order in memory (first index varies the fastest).
         F order means that column-wise operations will be faster. 
dtype : [optional, float(byDeafult)] Data type of returned array.  

```

**代码#1:**

```py
# Python Program to create array with all ones
import numpy as geek 

a = geek.ones(3, dtype = int) 
print("Matrix a : \n", a) 

b = geek.ones([3, 3], dtype = int) 
print("\nMatrix b : \n", b) 
```

**输出:**

```py
Matrix a : 
 [1 1 1]

Matrix b : 
 [[1 1 1]
 [1 1 1]
 [1 1 1]]

```

**代码#2:**

```py
# Python Program to create array with all ones
import numpy as geek 

c = geek.ones([5, 3]) 
print("\nMatrix c : \n", c) 

d = geek.ones([5, 2], dtype = float) 
print("\nMatrix d : \n", d) 
```

**输出:**

```py
Matrix c : 
 [[ 1\.  1\.  1.]
 [ 1\.  1\.  1.]
 [ 1\.  1\.  1.]
 [ 1\.  1\.  1.]
 [ 1\.  1\.  1.]]

Matrix d : 
 [[ 1\.  1.]
 [ 1\.  1.]
 [ 1\.  1.]
 [ 1\.  1.]
 [ 1\.  1.]]

```