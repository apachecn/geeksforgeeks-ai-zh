# 用随机值创建 Numpy 数组| Python

> 原文:[https://www . geeksforgeeks . org/create-a-numpy-array-with-random-values-python/](https://www.geeksforgeeks.org/create-a-numpy-array-with-random-values-python/)

在本文中，我们将学习如何创建一个充满随机值的 Numpy 数组，给定数组的形状和类型。

我们可以使用 Numpy.empty()方法来完成这个任务。该方法采用三个参数，讨论如下–

```
-> shape : Number of rows
-> order : C_contiguous or F_contiguous
-> dtype : [optional, float(by Default)] Data type of returned array. 

```

**示例#1:**

```
# Python Program to create numpy array 
# filled with random values
import numpy as geek 

b = geek.empty(2, dtype = int) 
print("Matrix b : \n", b) 

a = geek.empty([2, 2], dtype = int) 
print("\nMatrix a : \n", a) 
```

输出:

```
Matrix b : 
 [140489599921032        21301024]

Matrix a : 
 [[140489599921048        18650592]
 [       10738656 140489568798064]]

```

**例 2:**

```
# Python Program to create numpy array 
# filled with random values
import numpy as geek 

# Python Program to create numpy array 
# filled with random values
import numpy as geek 

c = geek.empty([3, 3]) 
print("\nMatrix c : \n", c)

d = geek.empty([5, 3], dtype = int) 
print("\nMatrix d : \n", d)

```

**输出:**

```
Matrix c : 
 [[  1.37596097e-316   5.39314154e-317   5.39307830e-317]
 [  5.39345774e-317   5.39345774e-317   6.93325440e-310]
 [  5.39481741e-317   6.93325440e-310   8.69555537e-322]]

Matrix d : 
 [[140330665569272        23735792               0]
 [       10739936 140330589556496               0]
 [              0               0        10739904]
 [140330587337872               0        10915968]
 [              0        10739904               0]]

```