# 创建一个用全零填充的 Numpy 数组| Python

> 原文:[https://www . geeksforgeeks . org/create-a-numpy-array-全零填充-python/](https://www.geeksforgeeks.org/create-a-numpy-array-filled-with-all-zeros-python/)

在本文中，我们将学习如何创建一个充满全零的 Numpy 数组，给定数组的形状和类型。

我们可以使用 Numpy.zeros()方法来完成这个任务。该方法采用三个参数，讨论如下–

```
shape : integer or sequence of integers
order  : C_contiguous or F_contiguous
         C-contiguous order in memory(last index varies the fastest)
         C order means that operating row-rise on the array will be slightly quicker
         FORTRAN-contiguous order in memory (first index varies the fastest).
         F order means that column-wise operations will be faster. 
dtype : [optional, float(byDeafult)] Data type of returned array.  

```

**示例#1:**

```
# Python Program to create array with all zeros
import numpy as geek 

a = geek.zeros(3, dtype = int) 
print("Matrix a : \n", a) 

b = geek.zeros([3, 3], dtype = int) 
print("\nMatrix b : \n", b) 
```

**输出:**

```
Matrix a : 
 [0 0 0]

Matrix b : 
 [[0 0 0]
 [0 0 0]
 [0 0 0]]

```

**例 2:**

```
# Python Program to create array with all zeros
import numpy as geek 

c = geek.zeros([5, 3]) 
print("\nMatrix c : \n", c) 

d = geek.zeros([5, 2], dtype = float) 
print("\nMatrix d : \n", d) 
```

**输出:**

```
Matrix c : 
 [[ 0\.  0\.  0.]
 [ 0\.  0\.  0.]
 [ 0\.  0\.  0.]
 [ 0\.  0\.  0.]
 [ 0\.  0\.  0.]]

Matrix d : 
 [[ 0\.  0.]
 [ 0\.  0.]
 [ 0\.  0.]
 [ 0\.  0.]
 [ 0\.  0.]]

```