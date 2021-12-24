# 如何用 Python 中的 NumPy 得到矩阵的维数？

> 原文:[https://www . geeksforgeeks . org/如何使用 python 中的 numpy 获得矩阵的维数/](https://www.geeksforgeeks.org/how-to-get-the-number-of-dimensions-of-a-matrix-using-numpy-in-python/)

在本文中，我们将讨论如何使用 [NumPy](https://www.geeksforgeeks.org/numpy-in-python-set-1-introduction/) 获得矩阵的维数。可以使用 [**ndarray()**](https://www.geeksforgeeks.org/numpy-ndarray/) 方法的 [**ndim**](https://www.geeksforgeeks.org/numpy-ndarray-ndim-method-python/) 参数找到它。

> **语法:**no _ of _ dimensions = numpy . ndarray . ndim

**进场:**

*   使用 numpy 包创建 n 维矩阵。
*   使用 numpy 数组可用的 *ndim* 属性作为 *numpy_array_name.ndim* 来获取维数。
*   或者，我们可以使用 *shape* 属性获取每个维度的大小，然后使用 *len()* 函数获取维度的数量。
*   使用 numpy.array()函数将列表转换为 numpy 数组，并使用上述两种方法之一获取维数。

**例 1:**

## 蟒蛇 3

```
import numpy as np

x = np.arange(12).reshape((3, 4))

print(x.ndim)
```

**输出:**

```
2
```

**例 2:**

## 蟒蛇 3

```
import numpy as np

# create numpy arrays
# 1-d numpy array
_1darr = np.arange(4)      

# 2-d numpy array
_2darr = np.arange(15).reshape((5, 3))     

# 3-d numpy array
_3darr = np.arange(18).reshape((3, 2, 3))  

# printing the type of value obtained using 
# attribute 'ndim'
print("Type of value obtained: ", type(_1darr.ndim))

# printing the dimensions of each numpy array
print("Dimensions in _1darr are: ", _1darr.ndim)
print("Dimensions in _2darr are: ", _2darr.ndim)
print("Dimensions in _3darr are: ", _3darr.ndim)

# numpy_arr.shape is the number of elements in
# each dimension numpy_arr.shape returns a tuple
# len() of the returned tuple is also gives number
# of dimensions
print("Dimensions in _3darr are: ", len(_3darr.shape))

# Use numpy.array() function to convert a list to
# numpy array
__1darr = np.array([5, 4, 1, 3, 2])
__2darr = np.array([[5, 4],[1,2], [4,5]])
print("Dimensions in __1darr are: ", __1darr.ndim)
print("Dimensions in __2darr are: ", __2darr.ndim)
```

**输出:**

```
Type of value obtained:  <class 'int'>
Dimensions in _1darr are:  1
Dimensions in _2darr are:  2
Dimensions in _3darr are:  3
Dimensions in _3darr are:  3
Dimensions in __1darr are:  1
Dimensions in __2darr are:  2
```