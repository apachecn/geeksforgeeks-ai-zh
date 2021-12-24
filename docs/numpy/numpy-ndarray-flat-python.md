# python 中的 numpy . ndarray . flat()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ndaarray-flat python/

**numpy.ndarray.flat()** 函数用作一维数组的一维迭代器。
它不是 Python 内置迭代器对象的子类，否则它就是一个 **numpy.flatiter** 实例。
**语法:**

```
numpy.ndarray.flat()
```

**参数:**

```
index : [tuple(int)] index of the values to iterate
```

**返回:**

```
1-D iteration of array
```

**代码 1:正在处理 2D 阵**

## 计算机编程语言

```
# Python Program illustrating
# working of ndarray.flat()

import numpy as geek

# Working on 1D iteration of 2D array
array = geek.arange(15).reshape(3, 5)
print("2D array : \n",array )

# Using flat() : 1D iterator over range
print("\nUsing Array : ", array.flat[2:6])

# Using flat() to Print 1D represented array
print("\n1D representation of array : \n ->", array.flat[0:15])
```

**输出:**

```
2D array : 
 [[ 0  1  2  3  4]
 [ 5  6  7  8  9]
 [10 11 12 13 14]]

Using Array :  [2 3 4 5]

1D representation of array : 
 -> [ 0  1  2 ..., 12 13 14]
```

**代码 2:改变数组**
的值

## 计算机编程语言

```
# Python Program illustrating
# working of ndarray.flat()

import numpy as geek

# Working on 1D iteration of 2D array
array = geek.arange(15).reshape(3, 5)
print("2D array : \n",array )

# All elements set to 1
array.flat = 1
print("\nAll Values set to 1 : \n", array)

array.flat[3:6] = 8
array.flat[8:10] = 9
print("Changing values in a range : \n", array)   
```

**输出:**

```
2D array : 
 [[ 0  1  2  3  4]
 [ 5  6  7  8  9]
 [10 11 12 13 14]]

All Values set to 1 : 
 [[1 1 1 1 1]
 [1 1 1 1 1]
 [1 1 1 1 1]]

Changing values in a range : 
 [[1 1 1 8 8]
 [8 1 1 9 9]
 [1 1 1 1 1]]
```

**numpy . flat ITER 实际上是什么？**
flat ITER 迭代器由 x.flat 为任何数组 x 返回。它允许在 N 维数组上进行迭代(以行为主的方式)，要么在 for 循环中进行迭代，要么调用其下一个方法。
**代码 3:numpy . flatter()**
角色

## 计算机编程语言

```
# Python Program illustrating
# working of ndarray.flat()

import numpy as geek

# Working on 1D iteration of 2D array
array = geek.arange(15).reshape(3, 5)
print("2D array : \n",array )

print("\nID array : \n", array.flat[0:15])        

print("\nType of array,flat() : ", type(array.flat))

for i in array.flat:
    print(i, end = ' ')
```

**输出:**

```
2D array : 
 [[ 0  1  2  3  4]
 [ 5  6  7  8  9]
 [10 11 12 13 14]]

ID array : 
 [ 0  1  2 ..., 12 13 14]

Type of array,flat() :  
0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 
```

**参考文献:**
[https://docs . scipy . org/doc/numpy/reference/generated/numpy . ndarray . flat . html # numpy . ndarray . flat](https://docs.scipy.org/doc/numpy/reference/generated/numpy.ndarray.flat.html#numpy.ndarray.flat)
**注:**
这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作。
本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。