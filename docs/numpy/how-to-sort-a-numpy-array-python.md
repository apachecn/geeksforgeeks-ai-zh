# 如何对 Numpy 数组进行排序| Python

> 原文:[https://www . geeksforgeeks . org/how-sort-a-numpy-array-python/](https://www.geeksforgeeks.org/how-to-sort-a-numpy-array-python/)

在本文中，我们将学习如何对 Numpy 数组进行排序。根据需求，Numpy 中有多种方法对数组进行排序。让我们借助例子来试着理解它们。

**示例#1:** 使用 sort()方法基于轴对给定数组进行简单排序。

```py
# importing libraries
import numpy as np

# sort along the first axis
a = np.array([[12, 15], [10, 1]])
arr1 = np.sort(a, axis = 0)        
print ("Along first axis : \n", arr1)        

# sort along the last axis
a = np.array([[10, 15], [12, 1]])
arr2 = np.sort(a, axis = -1)        
print ("\nAlong first axis : \n", arr2)

a = np.array([[12, 15], [10, 1]])
arr1 = np.sort(a, axis = None)        
print ("\nAlong none axis : \n", arr1)
```

**输出:**

```py
Along first axis : 
 [[10  1]
 [12 15]]

Along first axis : 
 [[10 15]
 [ 1 12]]

Along none axis : 
 [ 1 10 12 15]

```

**示例#2:** 使用 argsort()方法获取可以返回排序数组的索引

```py
# Python code to demonstrate 
# working of  numpy.argsort
import numpy as np

# Numpy array created
a = np.array([9, 3, 1, 7, 4, 3, 6])

# unsorted array print
print('Original array:\n', a)

# Sort array indices
b = np.argsort(a)
print('Sorted indices of original array->', b)

# To get sorted array using sorted indices
# c is temp array created of same len as of b
c = np.zeros(len(b), dtype = int)
for i in range(0, len(b)):
    c[i]= a[b[i]]
print('Sorted array->', c)
```

**输出:**

```py
Original array:
 [9 3 1 7 4 3 6]
Sorted indices of original array-> [2 1 5 4 6 3 0]
Sorted array-> [1 3 3 4 6 7 9]

```

**示例#3:** 使用一系列键获得稳定的排序。

```py
import numpy as np

# Numpy array created
# First column
a = np.array([9, 3, 1, 3, 4, 3, 6])

# Second column 
b = np.array([4, 6, 9, 2, 1, 8, 7]) 
print('column a, column b')
for (i, j) in zip(a, b):
    print(i, ' ', j)

# Sort by a then by b
ind = np.lexsort((b, a)) 
print('Sorted indices->', ind)
```

**输出:**

```py
column a, column b
9   4
3   6
1   9
3   2
4   1
3   8
6   7
Sorted indices-> [2 3 1 5 4 6 0]

```