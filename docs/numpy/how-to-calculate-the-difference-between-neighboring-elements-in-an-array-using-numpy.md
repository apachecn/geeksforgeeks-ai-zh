# 如何使用 NumPy

计算数组中相邻元素之间的差异

> 原文:[https://www . geeksforgeeks . org/如何使用-numpy/](https://www.geeksforgeeks.org/how-to-calculate-the-difference-between-neighboring-elements-in-an-array-using-numpy/) 计算数组中相邻元素之间的差异

让我们看看如何使用 NumPy 库计算数组中相邻元素之间的差异。

所以，我们可以利用 numpy 库的 [**numpy.diff()**](https://www.geeksforgeeks.org/numpy-diff-in-python/) 功能找出相邻元素的区别。

> **语法:** numpy.diff(arr，n，axis)

现在，让我们看一个例子:

**例 1:**

## 蟒蛇 3

```
# import library
import numpy as np

# create a numpy 1d-array
arr = np.array([1, 12, 3, 14, 5,
              16, 7, 18, 9, 110])

# finding the difference between
# neighboring elements
result = np.diff(arr)

print(result)
```

**输出:** 

```
[ 11  -9  11  -9  11  -9  11  -9 101]
```

**例 2:**

## 蟒蛇 3

```
# import library
import numpy as np

# create a numpy 2d-array
arr = np.array([[10, 12, 14], 
                [25, 35, 45],
                [12, 18, 20]])

# finding the difference between
# neighboring elements along row
result = np.diff(arr, axis = 1)

print(result)
```

**输出:**

```
[[ 2  2]
[10 10]
[ 6  2]]
```

**例 3:**

## 蟒蛇 3

```
# import library
import numpy as np

# create a numpy 2d-array
arr = np.array([[10, 12, 14], 
                [25, 35, 45],
                [12, 18, 20]])

# finding the difference between
# neighboring elements along column
result = np.diff(arr, axis = 0)

print(result)
```

**输出:**

```
[[ 15  23  31]
[-13 -17 -25]]
```