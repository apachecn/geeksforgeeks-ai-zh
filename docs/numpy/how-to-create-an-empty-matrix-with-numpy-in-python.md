# 如何用 Python 中的 NumPy 创建一个空矩阵？

> 原文:[https://www . geeksforgeeks . org/如何用 python 中的 numpy 创建空矩阵/](https://www.geeksforgeeks.org/how-to-create-an-empty-matrix-with-numpy-in-python/)

术语**空矩阵**没有行也没有列。包含缺失值的矩阵至少有一行和一列，包含零的矩阵也是如此。**数值 Python(**[](https://www.geeksforgeeks.org/numpy-in-python-set-1-introduction/)****)**为 Python 中数值数组和矩阵的运算提供了丰富的有用特性和功能。如果你想借助 NumPy 创建一个空矩阵。我们可以使用一个函数:**

1.  ****空****
2.  **num py . zero**

****1。** **numpy.empty :** 返回给定形状和类型的新数组，不初始化条目。**

> ****语法:** numpy.empty(shape，dtype=float，order='C ')**
> 
>  ****参数:**
> 
> *   形状:int 或 int 的元组，即数组(5，6)或 5 的形状。
> *   数据类型数据类型，可选，即数组所需的输出数据类型，例如 numpy.int8。默认值为 umpy.float64。
> *   顺序{'C '，' F'}，可选，默认:' C '即在内存中是按行主(C 风格)还是列主(Fortran 风格)顺序存储多维数据。**

**让我们从 NumPy 中的空函数开始，考虑一个您想要创建一个 5×5 的空矩阵的例子**

****示例 1:** 要创建 5 列 0 行的空矩阵:**

## **蟒蛇 3**

```
import numpy as np

x = np.empty((0, 5))
print('The value is :', x)

# if we check the matrix dimensions 
# using shape:
print('The shape of matrix is :', x.shape)

# by default the matrix type is float64
print('The type of matrix is :', x.dtype)
```

****输出:****

```
The value is : []
The shape of matrix is : (0, 5)
The type of matrix is : float64
```

**这里，矩阵由 0 行和 5 列组成，这就是为什么结果是“[ ]”。让我们再举一个 NumPy 中的空函数的例子，考虑一个例子，你想用一些随机数创建一个空矩阵 4 x 2。**

****示例 2:** 使用预期的尺寸/大小初始化空数组:**

## **蟒蛇 3**

```
# import the library
import numpy as np

# Here 4 is the number of rows and 2 
# is the number of columns
y = np.empty((4, 2))

# print the matrix
print('The matrix is : \n', y)

# print the matrix consist of 25 random numbers
z = np.empty(25)

# print the matrix
print('The matrix with 25 random values:', z)
```