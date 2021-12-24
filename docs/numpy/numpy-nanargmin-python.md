# python 中的 numpy.nanargmin()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-nana rgmin-python/

**numpy.nanargmin()** 函数返回特定轴上数组的 min 元素的索引，忽略 NaNs。
如果切片只包含 NaNs 和 Infs，则结果不可信。

**语法:**

```
numpy.nanargmin(array, axis = None)
```

**参数:**

```
array : Input array to work on 
axis  : [int, optional]Along a specified axis like 0 or 1
```

**返回:**

```
Array of indices into the array with same shape as array.shape.
 with the dimension along axis removed.
```

**代码 1 :**

## 计算机编程语言

```
# Python Program illustrating
# working of nanargmin()

import numpy as geek

# Working on 1D array
array = [geek.nan, 4, 2, 3, 1]
print("INPUT ARRAY 1 : \n", array)

array2 = geek.array([[geek.nan, 4], [1, 3]])

# returning Indices of the min element
# as per the indices ingnoring NaN
print("\nIndices of min in array1 : ",
      geek.nanargmin(array))

# Working on 2D array
print("\nINPUT ARRAY 2 : \n", array2)
print("\nIndices of min in array2 : ",
      geek.nanargmin(array2))

print("\nIndices at axis 1 of array2 : ",
      geek.nanargmin(array2, axis = 1))
```

**输出:**

```
INPUT ARRAY 1 : 
 [nan, 4, 2, 3, 1]

Indices of min in array1 :  4

INPUT ARRAY 2 : 
 [[ nan   4.]
 [  1\.   3.]]

Indices of min in array2 :  2

Indices at axis 1 of array2 :  [1 0]
```

**代码 2:比较 argmin 和 nanargmin 的工作情况**

## 计算机编程语言

```
# Python Program illustrating
# working of nanargmin()

import numpy as geek

# Working on 2D array
array = ( [[ 8, 13, 5, 0],
           [ geek.nan, geek.nan, 5, 3],
           [10, 7, 15, 15],
           [3, 11, 4, 12]])
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

print("\nIndices of min using argmin : ",
      geek.argmin(array, axis = 0))
print("\nIndices of min using nanargmin :  : ",
      geek.nanargmin(array, axis = 0))
```

**输出:**

```
INPUT ARRAY : 
 [[ 8 13  5  0]
 [ 0  2  5  3]
 [10  7 15 15]
 [ 3 11  4 12]]

Indices of min element :  [1 1 3 0]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . nanargmin . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.nanargmin.html)
**注:**
这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作方式
。
本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。