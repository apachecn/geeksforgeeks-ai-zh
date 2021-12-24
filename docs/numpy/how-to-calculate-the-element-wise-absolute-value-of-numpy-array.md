# 如何计算 NumPy 数组的元素绝对值？

> 原文:[https://www . geeksforgeeks . org/如何按元素计算 numpy 数组的绝对值/](https://www.geeksforgeeks.org/how-to-calculate-the-element-wise-absolute-value-of-numpy-array/)

让我们看看寻找 NumPy 数组元素绝对值的程序。为了完成这个任务，我们使用了 numpy 库的 [**numpy.absolute()**](https://www.geeksforgeeks.org/numpy-absolute-python/) 功能。这个数学函数有助于计算数组中每个元素的绝对值。

> **语法:** numpy.absolute(arr，out = None，ufunc 'absolute ')
> 
> **返回:**每个元素绝对值的数组。

让我们看一个例子:

**例 1:** 一维数组的元素绝对值。

## 蟒蛇 3

```py
# import library
import numpy as np

# create a numpy 1d-array
array = np.array([1, -2, 3])

print("Given array:\n", array)

# find element-wise
# absolute value
rslt = np.absolute(array)

print("Absolute array:\n", rslt)
```

**输出:**

```py
Given array:
[ 1 -2  3]
Absolute array:
[1 2 3]

```

**例 2:** 二维数组的元素绝对值。

## 蟒蛇 3

```py
# import library
import numpy as np

# create a numpy 2d-array
array = np.array([[1, -2, 3],
                  [-4, 5, -6]])

print("Given array:\n",
      array)

# find element-wise
# absolute value
rslt = np.absolute(array)

print("Absolute array:\n",
      rslt)
```

**输出:**

```py
Given array:
[[ 1 -2  3]
[-4  5 -6]]
Absolute array:
[[1 2 3]
[4 5 6]]

```

**例 3:** 三维数组的元素绝对值。

## 蟒蛇 3

```py
# import library
import numpy as np

# create a numpy 3d-array
array = np.array([
    [[1, -2, 3],
     [-4, 5, -6]],

    [[-7.5, -8.22, 9.0],
     [10.0, 11.5, -12.5]]
                 ])

print("Given array:\n",
      array)

# find element-wise
# absolute value 
rslt = np.absolute(array)

print("Absolute array:\n",
      rslt)
```

**输出:**

```py
Given array:
[[[  1\.    -2\.     3\.  ]
 [ -4\.     5\.    -6\.  ]]

[[ -7.5   -8.22   9\.  ]
 [ 10\.    11.5  -12.5 ]]]
Absolute array:
[[[ 1\.    2\.    3\.  ]
 [ 4\.    5\.    6\.  ]]

[[ 7.5   8.22  9\.  ]
 [10\.   11.5  12.5 ]]]

```