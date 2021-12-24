# Python |反转 numpy 数组

> 原文:[https://www.geeksforgeeks.org/python-reverse-a-numpy-array/](https://www.geeksforgeeks.org/python-reverse-a-numpy-array/)

我们知道 [Numpy](https://www.geeksforgeeks.org/numpy-in-python-set-1-introduction/) 是一个通用的数组处理包，它提供了一个高性能的多维数组对象，以及使用这些数组的工具。让我们讨论一下如何反转 numpy 数组。

**方法一:使用快捷方法**

```
# Python code to demonstrate
# how to reverse numpy array
# using shortcut method

import numpy as np

# initialising numpy array
ini_array = np.array([1, 2, 3, 6, 4, 5])

# printing initial ini_array
print("initial array", str(ini_array))

# printing type of ini_array
print("type of ini_array", type(ini_array))

# using shortcut method to reverse
res = ini_array[::-1]

# printing result
print("final array", str(res))
```

**输出:**

```
initial array [1 2 3 6 4 5]
type of ini_array <class 'numpy.ndarray'>
final array [5 4 6 3 2 1]

```

**方法 2:使用`flipud`功能**

```
# Python code to demonstrate
# how to reverse numpy array
# using flipud method

import numpy as np

# initialising numpy array
ini_array = np.array([1, 2, 3, 6, 4, 5])

# printing initial ini_array
print("initial array", str(ini_array))

# printing type of ini_array
print("type of ini_array", type(ini_array))

# using flipud method to reverse
res = np.flipud(ini_array)

# printing result
print("final array", str(res))
```

**输出:**

```
initial array [1 2 3 6 4 5]
type of ini_array <class 'numpy.ndarray'>
final array [5 4 6 3 2 1]

```