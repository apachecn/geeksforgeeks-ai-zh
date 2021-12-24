# Python 中的 numpy.delete()

> 原文:[https://www.geeksforgeeks.org/numpy-delete-python/](https://www.geeksforgeeks.org/numpy-delete-python/)

**numpy.delete()** 函数返回一个新数组，并删除子数组以及所提到的轴。

**语法:**

```py
numpy.delete(array, object, axis = None)
```

**参数:**

```py
array   : [array_like]Input array. 
object  : [int, array of ints]Sub-array to delete
axis    : Axis along which we want to delete sub-arrays. By default, it object is applied to  
                flattened array

```

**返回:**

```py
An array with sub-array being deleted as per the mentioned object along a given axis. 

```

**代码 1:从 1D 阵**删除

## 计算机编程语言

```py
# Python Program illustrating
# numpy.delete()

import numpy as geek

#Working on 1D
arr = geek.arange(5)
print("arr : \n", arr)
print("Shape : ", arr.shape)

# deletion from 1D array 

object = 2
a = geek.delete(arr, object)
print("\ndeleteing {} from array : \n {}".format(object,a))
print("Shape : ", a.shape)

object = [1, 2]
b = geek.delete(arr, object)
print("\ndeleteing {} from array : \n {}".format(object,a))
print("Shape : ", a.shape)
```

**输出:**

```py
arr : 
 [0 1 2 3 4]
Shape :  (5,)

deleteing arr 2 times : 
 [0 1 3 4]
Shape :  (4,)

deleteing arr 3 times : 
 [0 3 4]
Shape :  (4,)

```

**代码 2 :**

## 计算机编程语言

```py
# Python Program illustrating
# numpy.delete()

import numpy as geek

#Working on 1D
arr = geek.arange(12).reshape(3, 4)
print("arr : \n", arr)
print("Shape : ", arr.shape)

# deletion from 2D array 
a = geek.delete(arr, 1, 0)
'''
        [[ 0  1  2  3]
         [ 4  5  6  7] -> deleted
         [ 8  9 10 11]]
'''
print("\ndeleteing arr 2 times : \n", a)
print("Shape : ", a.shape)

# deletion from 2D array 
a = geek.delete(arr, 1, 1)
'''
        [[ 0  1*  2  3]
         [ 4  5*  6  7] 
         [ 8  9* 10 11]]
              ^
              Deletion
'''
print("\ndeleteing arr 2 times : \n", a)
print("Shape : ", a.shape)
```

**输出:**

```py
arr : 
 [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]
Shape :  (3, 4)

deleteing arr 2 times : 
 [[ 0  1  2  3]
 [ 8  9 10 11]]
Shape :  (2, 4)

deleteing arr 2 times : 
 [[ 0  2  3]
 [ 4  6  7]
 [ 8 10 11]]
Shape :  (3, 3)

deleteing arr 3 times : 
 [ 0  3  4  5  6  7  8  9 10 11]
Shape :  (3, 3)

```

**代码 3:使用布尔掩码**
执行删除

## 计算机编程语言

```py
# Python Program illustrating
# numpy.delete()

import numpy as geek

arr = geek.arange(5)
print("Original array : ", arr)
mask = geek.ones(len(arr), dtype=bool)

# Equivalent to np.delete(arr, [0,2,4], axis=0)
mask[[0,2]] = False
print("\nMask set as : ", mask)
result = arr[mask,...]
print("\nDeletion Using a Boolean Mask : ", result)
```

**输出:**

```py
Original array :  [0 1 2 3 4]

Mask set as :  [False  True False  True  True]

Deletion Using a Boolean Mask :  [1 3 4]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy/reference/generated/numpy . delete . html](https://docs.scipy.org/doc/numpy/reference/generated/numpy.delete.html)
**注意:**
这些代码不会在 online-ID 上运行。请在您的系统上运行它们来探索工作方式
。
本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。