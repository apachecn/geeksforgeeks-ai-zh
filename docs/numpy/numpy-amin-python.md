# python 中的 numpy.amin()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-Amin-python/

**numpy.amin()** 函数返回数组的最小值或沿轴的最小值(如果提到的话)。

**语法:** numpy.amin(arr，axis = None，out = None，keepdims = < class numpy。_ 全局。_NoValue >)

**参数:**

*   **arr:**【array _ like】输入数据
*   **轴:**【int 或 int 的元组】轴，我们要沿着它取最小值。否则，它将认为 arr 被展平。
*   **输出:**【n 数组，可选】放置结果的备选输出数组
*   **保留尺寸:**【布尔型，可选】如果设置为真，则减少的轴将作为尺寸为 1 的尺寸留在
    结果中。使用该选项，结果将根据输入数组
    正确广播。如果传递了默认值，则 keepdims 不会传递到 ndarray 子类的 all
    方法，但是任何非默认值都将传递。如果子类求和方法
    不实现 keepdims，将会引发任何异常。

**返回:**

数组的最小值–arr[n 数组或标量]，如果轴为无，则为标量；
如果提到轴，结果是维度 a . ndim–1 的数组。

**代码–**

```
# Python Program illustrating
# numpy.amin() method

import numpy as geek

# 1D array
arr = geek.arange(8)
print("arr : ", arr)
print("Min of arr : ", geek.amin(arr))

# 2D array
arr = geek.arange(10).reshape(2, 5)
print("\narr : ", arr)

# Minimum of the flattened array
print("\nMin of arr, axis = None : ", geek.amin(arr))

# Minimum along the first axis
# axis 0 means vertical
print("Min of arr, axis = 0 : ", geek.amin(arr, axis = 0))

# Minimum along the second axis
# axis 1 means horizontal
print("Min of arr, axis = 1 : ", geek.amin(arr, axis = 1))   
```

**输出–**

```
arr :  [0 1 2 3 4 5 6 7]
Min of arr :  0

arr :  [[0 1 2 3 4]
 [5 6 7 8 9]]

Min of arr, axis = None :  0
Min of arr, axis = 0 :  [0 1 2 3 4]
Min of arr, axis = 1 :  [0 5]

```

**References–**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . Amin . html # numpy . Amin](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.amin.html#numpy.amin)

**注意–**
这些代码不会在在线 ID 上运行。请在您的系统上运行它们来探索工作的
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。