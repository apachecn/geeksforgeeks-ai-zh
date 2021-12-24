# Python 中 numpy.apply _ 沿 _ 轴()

> 原文:[https://www . geesforgeks . org/numpy-apply _ along _ axis-python/](https://www.geeksforgeeks.org/numpy-apply_along_axis-python/)

**numpy . apply _ long _ axis()**函数帮助我们对给定数组的 1D 切片应用所需的函数。
T3】1d _ func(ar，*args) : 在一维数组上工作，其中 **ar** 是 **arr** 沿轴的 1d 切片。

**语法:**

```
numpy.apply_along_axis(1d_func, axis, array, *args, **kwargs) 
```

**参数:**

```
1d_func  : the required function to perform over 1D array. It can only be applied in 
         1D slices of input array and that too along a particular axis. 
axis     : required axis along which we want input array to be sliced
array    : Input array to work on 
*args    : Additional arguments to 1D_function 
**kwargs : Additional arguments to 1D_function  
```

**args 和**kwargs 实际上是什么？**

这两种方式都允许您向函数传递可变数量的参数。
***args :** 允许向函数发送非关键字变长参数列表。

## 计算机编程语言

```
# Python Program illustrating
# use of *args

args = [3, 8]
a = list(range(*args))
print("use of args  : \n   ", a)
```

**输出:**

```
use of args  : 
    [3, 4, 5, 6, 7]
```

****kwargs:** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。

## 计算机编程语言

```
# Python Program illustrating
# use of **kwargs

def test_args_kwargs(in1, in2, in3):
    print ("in1:", in1)
    print ("in2:", in2)
    print ("in3:", in3)

kwargs = {"in3": 1, "in2": "No.","in1":"geeks"}
test_args_kwargs(**kwargs)
```

**输出:**

```
in1: geeks
in2: No.
in3: 1
```

**代码 1:解释 numpy.apply _ 沿 _ 轴()用法的 Python 代码。**

## 计算机编程语言

```
# Python Program illustrating
# apply_along_axis() in NumPy

import numpy as geek

# 1D_func is "geek_fun"
def geek_fun(a):
    # Returning the sum of elements at start index and at last index
    # inout array
     return (a[0] + a[-1])

arr = geek.array([[1,2,3],
                [4,5,6],
                [7,8,9]])

'''
              -> [1,2,3] <-   1 + 7
                 [4,5,6]      2 + 8
              -> [7,8,9] <-   3 + 9
'''
print("axis=0 : ", geek.apply_along_axis(geek_fun, 0, arr))
print("\n")

'''             |   |
               [1,2,3]   1 + 3
               [4,5,6]   4 + 6
               [7,8,9]   7 + 9
                ^   ^              
'''
print("axis=1 : ", geek.apply_along_axis(geek_fun, 1, arr))
```

**输出:**

```
axis=0 :  [ 8 10 12]

axis=1 :  [ 4 10 16]
```

**代码 2:使用 NumPy Python 中的 apply_along_axis()进行排序**

## 计算机编程语言

```
# Python Program illustrating
# apply_along_axis() in NumPy

import numpy as geek

geek_array = geek.array([[8,1,7],
                         [4,3,9],
                         [5,2,6]])

# using pre-defined sorted function as 1D_func
print("Sorted as per axis 1 : \n", geek.apply_along_axis(sorted, 1, geek_array))

print("\n")

print("Sorted as per axis 0 : \n", geek.apply_along_axis(sorted, 0, geek_array))
```

**输出:**

```
Sorted as per axis 1 : 
 [[1 7 8]
 [3 4 9]
 [2 5 6]]

Sorted as per axis 0 : 
 [[4 1 6]
 [5 2 7]
 [8 3 9]]
```

**注意:**
这些 NumPy-Python 程序不会在 onlineID 上运行，所以在你的系统上运行它们来探索它们。

本文由**莫希特·古普塔 _OMG 供稿😀**。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。