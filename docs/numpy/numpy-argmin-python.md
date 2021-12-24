# numpy.argmin()用 Python

表示

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-argmin-python/

**numpy.argmin()** 方法返回特定轴上数组的 min 元素的索引。

**语法:**

```py
numpy.argmin(array, axis = None, out = None)
```

**参数:**

```py
array : Input array to work on 
axis  : [int, optional]Along a specified axis like 0 or 1
out   : [array optional]Provides a feature to insert output to the out
          array and it should be of appropriate shape and dtype
```

**返回:**

```py
Array of indices into the array with same shape as array.shape
 with the dimension along axis removed.
```

**代码 1 :**

## 计算机编程语言

```py
# Python Program illustrating
# working of argmin()

import numpy as geek

# Working on 1D array
array = geek.arange(8)
print("INPUT ARRAY : \n", array)

# returning Indices of the min element
# as per the indices
print("\nIndices of min element : ", geek.argmin(array, axis=0))
```

**输出:**

```py
INPUT ARRAY : 
 [0 1 2 3 4 5 6 7]

Indices of min element :  0
```

**代码 2 :**

## 计算机编程语言

```py
# Python Program illustrating
# working of argmin()

import numpy as geek

# Working on 2D array
array =  geek.random.randint(16, size=(4, 4))
print("INPUT ARRAY : \n", array)

# returning Indices of the min element
# as per the indices

'''  
   [[ 8 13  5  0]
   [ 0  2  5  3]
   [10  7 15 15]
   [ 3 11  4 12]]
     ^  ^  ^  ^
     0  2  4  0  - element
     1  1  3  0  - indices
'''
print("\nIndices of min element : ", geek.argmin(array, axis = 0))
```

**输出:**

```py
INPUT ARRAY : 
 [[ 8 13  5  0]
 [ 0  2  5  3]
 [10  7 15 15]
 [ 3 11  4 12]]

Indices of min element :  [1 1 3 0]
```

**代码 3 :**

## 计算机编程语言

```py
# Python Program illustrating
# working of argmin()

import numpy as geek

# Working on 2D array
array =  geek.arange(10).reshape(2, 5)
print("array : \n", array)

array[0][0] = 10
array[1][1] = 1
array[0][1] = 1
print("\narray : \n", array)

# Returns min element
print("\narray : ", geek.argmin(array))

# First occurrence of an min element is given
print("\nmin ELEMENT INDICES : ", geek.argmin(array, axis = 0))
```

**输出:**

```py
array : 
 [[0 1 2 3 4]
 [5 6 7 8 9]]

array : 
 [[10  1  2  3  4]
 [ 5  1  7  8  9]]

array :  1

min ELEMENT INDICES :  [1 0 0 0 0]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . arg min . html # numpy . arg min](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.argmin.html#numpy.argmin)
**注意:**
这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作方式
。
本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。