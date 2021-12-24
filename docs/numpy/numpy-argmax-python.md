# numpy.argmax()用 Python

表示

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-argmax-python/

**numpy.argmax()** 函数返回数组中最大元素在特定轴上的索引。

**语法:**

```
numpy.argmax(array, axis = None, out = None)
```

**参数:**

```
array : Input array to work on 
axis  : [int, optional]Along a specified axis like 0 or 1
out   : [array optional]Provides a feature to insert output to the out
          array and it should be of appropriate shape and dtype
```

**返回:**

```
Array of indices into the array with same shape as array.shape
 with the dimension along axis removed.
```

**代码 1 :**

## 计算机编程语言

```
# Python Program illustrating
# working of argmax()

import numpy as geek

# Working on 2D array
array = geek.arrange(12).reshape(3, 4)
print("INPUT ARRAY : \n", array)

# No axis mentioned, so works on entire array
print("\nMax element : ", geek.argmax(array))

# returning Indices of the max element
# as per the indices
print("\nIndices of Max element : ", geek.argmax(array, axis=0))
print("\nIndices of Max element : ", geek.argmax(array, axis=1))
```

**输出:**

```
INPUT ARRAY : 
 [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]

Max element :  11

Indices of Max element :  [2 2 2 2]

Indices of Max element :  [3 3 3]
```

**代码 2 :**

## 计算机编程语言

```
# Python Program illustrating
# working of argmax()

import numpy as geek

# Working on 2D array
array =  geek.random.randint(16, size=(4, 4))
print("INPUT ARRAY : \n", array)

# No axis mentioned, so works on entire array
print("\nMax element : ", geek.argmax(array))

# returning Indices of the max element
# as per the indices

'''  
   [[ 0  3  8 13]
    [12 11  2 11]
    [ 5 13  8  3]
    [12 15  3  4]]
      ^  ^  ^  ^
     12 15  8  13  - element
     1  3   0  0   - indices
'''
print("\nIndices of Max element : ", geek.argmax(array, axis = 0))

'''  
                            ELEMENT   INDEX
   ->[[ 0  3  8 13]           13        3
    ->[12 11  2 11]           12        0
    ->[ 5 13  8  3]           13        1
    ->[12 15  3  4]]          15        1

'''
print("\nIndices of Max element : ", geek.argmax(array, axis = 1))
```

**输出:**

```
INPUT ARRAY : 
 [[ 0  3  8 13]
  [12 11  2 11]
  [ 5 13  8  3]
  [12 15  3  4]]

Max element :  15

Indices of Max element :  [1 3 0 0]

Indices of Max element :  [3 0 1 1]
```

**代码 3 :**

## 计算机编程语言

```
# Python Program illustrating
# working of argmax()

import numpy as geek

# Working on 2D array
array =  geek.arrange(10).reshape(2, 5)
print("array : \n", array)

array[0][1] = 6
print("\narray : \n", array)

# Returns max element
print("\narray : ", geek.argmax(array))

# First occurrence of an max element is given
print("\nMAX ELEMENT INDICES : ", geek.argmax(array, axis = 0))
```

**输出:**

```
array : 
 [[0 1 2 3 4]
 [5 6 7 8 9]]

array : 
 [[0 6 2 3 4]
 [5 6 7 8 9]]

array :  9

MAX ELEMENT INDICES :  [1 0 1 1 1]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . arg max . html # numpy . arg max](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.argmax.html#numpy.argmax)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。

本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。