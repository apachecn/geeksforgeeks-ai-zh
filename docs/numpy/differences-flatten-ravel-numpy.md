# 扁平()和松散()数值函数之间的差异

> 原文:[https://www . geesforgeks . org/differences-flat-ravel-numpy/](https://www.geeksforgeeks.org/differences-flatten-ravel-numpy/)

我们有两种类似的方法将数组转换成 1D 数组:扁平化()和松散化()

```
import numpy as np
a = np.array( [ (1,7,3,4),(3,2,4,1) ] )
#OUTPUT:
print( a.flatten() )
# [ 1,7,3,4,3,2,4,1 ] 
print ( a.ravel() )
# [ 1,7,3,4,3,2,4,1 ] 

```

问题出现在这里，为什么有两个 numpy 函数来完成同一个任务？

**扁平化()和拉威尔()的区别**

**a.ravel()** :
(i)仅返回原始数组的引用/视图
(ii)如果修改数组，您会注意到原始数组的值也发生了变化。
(三)拉威尔比拉平()更快，因为它不占用任何内存。
(iv) Ravel 是库级函数。

**a .扁平化()** :
(i)返回原数组副本
(ii)如果修改此数组的任何值，原数组的值不受影响。
(三)flat()比 ravel()相对慢，因为它占用内存。
(iv)展平是一种排列对象的方法。

让我们通过这个代码来检查差异

```
# Python code to differentiate
# between flatten and ravel in numpy
import numpy as np

# Create a numpy array
a = np.array([(1,2,3,4),(3,1,4,2)])

# Let's print the array a
print ("Original array:\n ") 
print(a)

# To check the dimension of array (dimension =2)
# ( and type is numpy.ndarray )
print ("Dimension of array-> " , (a.ndim))

print("\nOutput for RAVEL \n") 
# Convert nd array to 1D array
b = a.ravel()

# Ravel only passes a view of 
# original array to array 'b'
print(b)
b[0]=1000
print(b)

# Note here that value of original
# array 'a' at also a[0][0] becomes 1000
print(a)

# Just to check the dimension i.e. 1
# (and type is same numpy.ndarray )
print ("Dimension of array->" ,(b.ndim))

print("\nOutput for FLATTEN \n") 

# Convert nd array to 1D array
c = a.flatten()

# Flatten passes copy of
# original array to 'c'
print(c)
c[0]=0
print(c)

# Note that by changing
# value of c there is no
# affect on value of original
# array 'a'
print(a)

print ("Dimension of array-> " , (c.ndim))
```

```
OUTPUT:
Original array:

[[1 2 3 4]
 [3 1 4 2]]
Dimension of array->  2

Output for RAVEL 

[1 2 3 4 3 1 4 2]
[1000    2    3    4    3    1    4    2]
[[1000    2    3    4]
 [   3    1    4    2]]
Dimension of array-> 1

Output for FLATTEN 

[1000    2    3    4    3    1    4    2]
[0 2 3 4 3 1 4 2]
[[1000    2    3    4]
 [   3    1    4    2]]
Dimension of array->  1
```

本文由 **SHAURYA UPPAL** 供稿。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。