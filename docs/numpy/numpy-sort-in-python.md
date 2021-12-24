# Python 中的 numpy.sort()

> 原文:[https://www.geeksforgeeks.org/numpy-sort-in-python/](https://www.geeksforgeeks.org/numpy-sort-in-python/)

**numpy.sort() :** 这个函数返回一个数组的排序副本。

**参数:**

> **arr :** 待排序数组。
> **轴:**轴，我们需要沿着它开始排列。
> **顺序:**此参数指定首先比较哪些字段。
> **种类:** ['quicksort'{default}，' mergesort '，' heap sort ']排序算法。

**返回:**

```py
Sorted Array
```

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