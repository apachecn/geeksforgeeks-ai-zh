# Python 中的 NumPy |第 1 集(简介)

> 原文:[https://www . geesforgeks . org/numpy-in-python-set-1-introduction/](https://www.geeksforgeeks.org/numpy-in-python-set-1-introduction/)

本文将帮助您熟悉 Python 中广泛使用的数组处理库。

**什么是 NumPy？**
NumPy 是一个通用的数组处理包。它提供了一个高性能的多维数组对象，以及使用这些数组的工具。

它是使用 Python 进行科学计算的基本包。它包含各种功能，包括以下重要功能:

*   一个强大的 N 维数组对象
*   复杂的(广播)功能
*   用于集成 C/C++和 Fortran 代码的工具
*   有用的线性代数、傅立叶变换和随机数功能

除了其明显的科学用途，NumPy 还可以用作通用数据的高效多维容器。
可以使用 NumPy 定义任意数据类型，这允许 Numpy 与各种各样的数据库无缝且快速地集成。

**安装:**

*   **Mac** 和 **Linux** 用户可以通过 pip 命令安装 NumPy:

    ```
    pip install numpy
    ```

*   **Windows** 没有任何类似于 linux 或 mac 的包管理器。请从[这里](http://www.lfd.uci.edu/~gohlke/pythonlibs/#numpy)下载 NumPy 的预建 windows 安装程序(根据您的系统配置和 Python 版本)。
    然后手动安装软件包。

**注意:**下面讨论的所有示例都不会在**在线 IDE 上运行。**

**1。NumPy 中的数组:** NumPy 的主要对象是齐次多维数组。

*   它是一个元素表(通常是数字)，都是相同的类型，由一组正整数索引。
*   在 NumPy 中，尺寸被称为*轴*。斧数为*级*。
*   NumPy 的数组类叫做 **ndarray** 。又名**阵**。

**示例:**

```
[[ 1, 2, 3],
 [ 4, 2, 5]]
Here,
rank = 2 (as it is 2-dimensional or it has 2 axes)
first dimension(axis) length = 2, second dimension has length = 3
overall shape can be expressed as: (2, 3)
```

## 蟒蛇 3

```
# Python program to demonstrate 
# basic array characteristics
import numpy as np

# Creating array object
arr = np.array( [[ 1, 2, 3],
                 [ 4, 2, 5]] )

# Printing type of arr object
print("Array is of type: ", type(arr))

# Printing array dimensions (axes)
print("No. of dimensions: ", arr.ndim)

# Printing shape of array
print("Shape of array: ", arr.shape)

# Printing size (total number of elements) of array
print("Size of array: ", arr.size)

# Printing type of elements in array
print("Array stores elements of type: ", arr.dtype)
```

Output :

```
Array is of type:  
No. of dimensions:  2
Shape of array:  (2, 3)
Size of array:  6
Array stores elements of type:  int64
```

**2。数组创建:**在 NumPy 中创建数组的方式多种多样。

*   例如，您可以使用**数组**功能从常规 Python **[列表](https://www.geeksforgeeks.org/python-set-3-strings-lists-tuples-iterations/)** 或**元组**创建数组。结果数组的类型是从序列中元素的类型推导出来的。
*   通常，数组的元素最初是未知的，但是它的大小是已知的。因此，NumPy 提供了几个函数来创建带有**初始占位符内容**的数组。这使得增长阵列的必要性最小化，而增长阵列是一项昂贵的操作。
    **例如:**NP . zero、np.ones、np.full、np.empty 等。
*   为了创建数字序列，NumPy 提供了一个类似于 range 的函数，它返回数组而不是列表。
*   **间隔:**返回给定间隔内均匀间隔的值。**步骤**尺寸指定。
*   **linspace:** 返回给定间隔内均匀分布的值。**号**号元素被退回。
*   **重塑阵:**我们可以用**重塑**的方法重塑一个阵。考虑一个具有形状(a1，a2，a3，…，an)的数组。我们可以重塑它，并将其转换为另一个带形状的数组(b1，b2，b3，…，bM)。唯一需要的条件是:
    a1 x a2 x a3 … x aN = b1 x b2 x b3 … x bM。(即阵列的原始大小保持不变。)
*   **展平阵:**我们可以用**展平**的方法得到一个折叠成**一维**的阵副本。它接受*命令*参数。默认值为“C”(对于行主顺序)。对列主顺序使用“F”。

**注意:**创建数组时可以明确定义数组的类型。

## 蟒蛇 3

```
# Python program to demonstrate
# array creation techniques
import numpy as np

# Creating array from list with type float
a = np.array([[1, 2, 4], [5, 8, 7]], dtype = 'float')
print ("Array created using passed list:\n", a)

# Creating array from tuple
b = np.array((1 , 3, 2))
print ("\nArray created using passed tuple:\n", b)

# Creating a 3X4 array with all zeros
c = np.zeros((3, 4))
print ("\nAn array initialized with all zeros:\n", c)

# Create a constant value array of complex type
d = np.full((3, 3), 6, dtype = 'complex')
print ("\nAn array initialized with all 6s." 
            "Array type is complex:\n", d)

# Create an array with random values
e = np.random.random((2, 2))
print ("\nA random array:\n", e)

# Create a sequence of integers 
# from 0 to 30 with steps of 5
f = np.arange(0, 30, 5)
print ("\nA sequential array with steps of 5:\n", f)

# Create a sequence of 10 values in range 0 to 5
g = np.linspace(0, 5, 10)
print ("\nA sequential array with 10 values between"
                                        "0 and 5:\n", g)

# Reshaping 3X4 array to 2X2X3 array
arr = np.array([[1, 2, 3, 4],
                [5, 2, 4, 2],
                [1, 2, 0, 1]])

newarr = arr.reshape(2, 2, 3)

print ("\nOriginal array:\n", arr)
print ("Reshaped array:\n", newarr)

# Flatten array
arr = np.array([[1, 2, 3], [4, 5, 6]])
flarr = arr.flatten()

print ("\nOriginal array:\n", arr)
print ("Fattened array:\n", flarr)
```

Output :

```
Array created using passed list:
 [[ 1\.  2\.  4.]
 [ 5\.  8\.  7.]]

Array created using passed tuple:
 [1 3 2]

An array initialized with all zeros:
 [[ 0\.  0\.  0\.  0.]
 [ 0\.  0\.  0\.  0.]
 [ 0\.  0\.  0\.  0.]]

An array initialized with all 6s. Array type is complex:
 [[ 6.+0.j  6.+0.j  6.+0.j]
 [ 6.+0.j  6.+0.j  6.+0.j]
 [ 6.+0.j  6.+0.j  6.+0.j]]

A random array:
 [[ 0.46829566  0.67079389]
 [ 0.09079849  0.95410464]]

A sequential array with steps of 5:
 [ 0  5 10 15 20 25]

A sequential array with 10 values between 0 and 5:
 [ 0\.          0.55555556  1.11111111  1.66666667  2.22222222  2.77777778
  3.33333333  3.88888889  4.44444444  5\.        ]

Original array:
 [[1 2 3 4]
 [5 2 4 2]
 [1 2 0 1]]
Reshaped array:
 [[[1 2 3]
  [4 5 2]]

 [[4 2 1]
  [2 0 1]]]

Original array:
 [[1 2 3]
 [4 5 6]]
Fattened array:
 [1 2 3 4 5 6]
```

**3。数组索引:**了解数组索引的基础知识对于分析和操作数组对象非常重要。NumPy 提供了许多方法来进行数组索引。

*   **切片:**就像 python 中的列表一样，NumPy 数组也可以切片。由于数组可以是多维的，您需要为数组的每个维度指定一个切片。
*   **整数数组索引:**在该方法中，为每个维度传递列表进行索引。完成对应元素的一对一映射以构建新的任意数组。
*   **布尔数组索引:**当我们想要从数组中挑选满足某个条件的元素时，使用这个方法。

## 蟒蛇 3

```
# Python program to demonstrate
# indexing in numpy
import numpy as np

# An exemplar array
arr = np.array([[-1, 2, 0, 4],
                [4, -0.5, 6, 0],
                [2.6, 0, 7, 8],
                [3, -7, 4, 2.0]])

# Slicing array
temp = arr[:2, ::2]
print ("Array with first 2 rows and alternate"
                    "columns(0 and 2):\n", temp)

# Integer array indexing example
temp = arr[[0, 1, 2, 3], [3, 2, 1, 0]]
print ("\nElements at indices (0, 3), (1, 2), (2, 1),"
                                    "(3, 0):\n", temp)

# boolean array indexing example
cond = arr > 0 # cond is a boolean array
temp = arr[cond]
print ("\nElements greater than 0:\n", temp)
```

Output :

```
Array with first 2 rows and alternatecolumns(0 and 2):
 [[-1\.  0.]
 [ 4\.  6.]]

Elements at indices (0, 3), (1, 2), (2, 1),(3, 0):
 [ 4\.  6\.  0\.  3.]

Elements greater than 0:
 [ 2\.   4\.   4\.   6\.   2.6  7\.   8\.   3\.   4\.   2\. ]
```

**4。基本操作:**NumPy 中提供了过多的内置算术函数。

*   **对单个数组的操作:**我们可以使用重载的算术运算符对数组进行元素式操作，创建一个新的数组。在+=、-=、*=运算符的情况下，现有数组将被修改。

## 蟒蛇 3

```
# Python program to demonstrate
# basic operations on single array
import numpy as np

a = np.array([1, 2, 5, 3])

# add 1 to every element
print ("Adding 1 to every element:", a+1)

# subtract 3 from each element
print ("Subtracting 3 from each element:", a-3)

# multiply each element by 10
print ("Multiplying each element by 10:", a*10)

# square each element
print ("Squaring each element:", a**2)

# modify existing array
a *= 2
print ("Doubled each element of original array:", a)

# transpose of array
a = np.array([[1, 2, 3], [3, 4, 5], [9, 6, 0]])

print ("\nOriginal array:\n", a)
print ("Transpose of array:\n", a.T)
```

Output :

```
Adding 1 to every element: [2 3 6 4]
Subtracting 3 from each element: [-2 -1  2  0]
Multiplying each element by 10: [10 20 50 30]
Squaring each element: [ 1  4 25  9]
Doubled each element of original array: [ 2  4 10  6]

Original array:
 [[1 2 3]
 [3 4 5]
 [9 6 0]]
Transpose of array:
 [[1 3 9]
 [2 4 6]
 [3 5 0]]

```

*   **一元运算符:**许多一元运算是作为**数组**类的方法提供的。这包括总和、最小值、最大值等。通过设置轴参数，也可以在行方向或列方向应用这些功能。

## 蟒蛇 3

```
# Python program to demonstrate
# unary operators in numpy
import numpy as np

arr = np.array([[1, 5, 6],
                [4, 7, 2],
                [3, 1, 9]])

# maximum element of array
print ("Largest element is:", arr.max())
print ("Row-wise maximum elements:",
                    arr.max(axis = 1))

# minimum element of array
print ("Column-wise minimum elements:",
                        arr.min(axis = 0))

# sum of array elements
print ("Sum of all array elements:",
                            arr.sum())

# cumulative sum along each row
print ("Cumulative sum along each row:\n",
                        arr.cumsum(axis = 1))
```

输出:

```
Largest element is: 9
Row-wise maximum elements: [6 7 9]
Column-wise minimum elements: [1 1 2]
Sum of all array elements: 38
Cumulative sum along each row:
[[ 1  6 12]
 [ 4 11 13]
 [ 3  4 13]]

```

*   **二进制运算符:**这些操作在数组元素中应用，并创建一个新数组。您可以使用所有基本的算术运算符，如+、-、/、*等。如果是+=，-=，* =运算符，则修改现有数组。

## 蟒蛇 3

```
# Python program to demonstrate
# binary operators in Numpy
import numpy as np

a = np.array([[1, 2],
            [3, 4]])
b = np.array([[4, 3],
            [2, 1]])

# add arrays
print ("Array sum:\n", a + b)

# multiply arrays (elementwise multiplication)
print ("Array multiplication:\n", a*b)

# matrix multiplication
print ("Matrix multiplication:\n", a.dot(b))
```

输出:

```
Array sum:
[[5 5]
 [5 5]]
Array multiplication:
[[4 6]
 [6 4]]
Matrix multiplication:
[[ 8  5]
 [20 13]]
```

*   **通用函数(ufunc):** NumPy 提供熟悉的数学函数，如 sin、cos、exp 等。这些函数还对数组进行元素操作，产生一个数组作为输出。

**注意:**上面我们用重载运算符做的所有操作都可以用像 np.add、np .减法、np .乘法、np.divide、np.sum 等 ufuncs 来完成。

## 蟒蛇 3

```
# Python program to demonstrate
# universal functions in numpy
import numpy as np

# create an array of sine values
a = np.array([0, np.pi/2, np.pi])
print ("Sine values of array elements:", np.sin(a))

# exponential values
a = np.array([0, 1, 2, 3])
print ("Exponent of array elements:", np.exp(a))

# square root of array values
print ("Square root of array elements:", np.sqrt(a))
```

Output:

```
Sine values of array elements: [  0.00000000e+00   1.00000000e+00   1.22464680e-16]
Exponent of array elements: [  1\.           2.71828183   7.3890561   20.08553692]
Square root of array elements: [ 0\.          1\.          1.41421356  1.73205081]
```

**4。排序数组:**有一个简单的 **np.sort** 方法对 NumPy 数组进行排序。让我们稍微探索一下。

## 蟒蛇 3

```
# Python program to demonstrate sorting in numpy
import numpy as np

a = np.array([[1, 4, 2],
                 [3, 4, 6],
              [0, -1, 5]])

# sorted array
print ("Array elements in sorted order:\n",
                    np.sort(a, axis = None))

# sort array row-wise
print ("Row-wise sorted array:\n",
                np.sort(a, axis = 1))

# specify sort algorithm
print ("Column wise sort by applying merge-sort:\n",
            np.sort(a, axis = 0, kind = 'mergesort'))

# Example to show sorting of structured array
# set alias names for dtypes
dtypes = [('name', 'S10'), ('grad_year', int), ('cgpa', float)]

# Values to be put in array
values = [('Hrithik', 2009, 8.5), ('Ajay', 2008, 8.7), 
           ('Pankaj', 2008, 7.9), ('Aakash', 2009, 9.0)]

# Creating array
arr = np.array(values, dtype = dtypes)
print ("\nArray sorted by names:\n",
            np.sort(arr, order = 'name'))

print ("Array sorted by grauation year and then cgpa:\n",
                np.sort(arr, order = ['grad_year', 'cgpa']))
```

Output:

```
Array elements in sorted order:
[-1  0  1  2  3  4  4  5  6]
Row-wise sorted array:
[[ 1  2  4]
 [ 3  4  6]
 [-1  0  5]]
Column wise sort by applying merge-sort:
[[ 0 -1  2]
 [ 1  4  5]
 [ 3  4  6]]

Array sorted by names:
[('Aakash', 2009, 9.0) ('Ajay', 2008, 8.7) ('Hrithik', 2009, 8.5)
 ('Pankaj', 2008, 7.9)]
Array sorted by grauation year and then cgpa:
[('Pankaj', 2008, 7.9) ('Ajay', 2008, 8.7) ('Hrithik', 2009, 8.5)
 ('Aakash', 2009, 9.0)]

```

所以，这是一个简单而简洁的 NumPy 库的介绍兼教程。
更详细的研究请参考 [NumPy 参考指南](https://docs.scipy.org/doc/numpy-1.10.1/reference/index.html)。
本文由 Nikhil Kumar 供稿。如果你喜欢极客博客并想投稿，你也可以用 write.geeksforgeeks.org 写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。