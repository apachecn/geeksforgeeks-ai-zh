# python 中的 numpy.amax()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-amax-python/

numpy.amax()方法返回数组的最大值或沿轴的最大值(如果提到的话)。

**语法:**

```py
numpy.amax(arr, axis = None, out = None, keepdims = <class numpy._globals._NoValue>)
```

**参数–**

*   **arr:**【array _ like】输入数据
*   **轴:**【int 或 int 的元组】我们想要最大值的轴。否则，它将认为 arr 被展平。
*   **out:**【n 数组，可选】放置结果的备选输出数组
*   **keepdmis :** 【布尔值，可选】如果设置为真，则减少的轴将作为尺寸为 1 的尺寸留在
    结果中。使用该选项，结果将根据输入数组
    正确广播。如果传递了默认值，则 keepdims 不会传递到 ndarray 子类的 all
    方法，但是任何非默认值都将传递。如果子类求和方法
    不实现 keepdims，将会引发任何异常。

**返回–**数组的最大值–arr[n 数组或标量]，如果轴为无，则为标量；如果提到 axis，结果是维度 a . ndim–1 的数组。

**代码–**

```py
# Python Program illustrating
# numpy.amax() method

import numpy as geek

# 1D array
arr = geek.arange(8)
print("arr : ", arr)
print("Max of arr : ", geek.amax(arr))

# 2D array
arr = geek.arange(10).reshape(2, 5)
print("\narr : ", arr)

# Maximum of the flattened array
print("\nMax of arr, axis = None : ", geek.amax(arr))

# Maxima along the first axis
# axis 0 means vertical
print("Max of arr, axis = 0 : ", geek.amax(arr, axis = 0))

# Maxima along the second axis
# axis 1 means horizontal
print("Max of arr, axis = 1 : ", geek.amax(arr, axis = 1))   
```

**输出–**

```py
arr :  [0 1 2 3 4 5 6 7]
Max of arr :  7

arr :  [[0 1 2 3 4]
 [5 6 7 8 9]]

Max of arr, axis = None :  9
Max of arr, axis = 0 :  [5 6 7 8 9]
Max of arr, axis = 1 :  [4 9]

```

**参考–**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/参考/生成/numpy.amax.html](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.amax.html)

**注意–**
这些代码不会在在线 ID 上运行。请在您的系统上运行它们来探索工作

本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。