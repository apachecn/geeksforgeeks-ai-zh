# 如何得到一个 3D NumPy 阵列的所有 2D 对角线？

> 原文:[https://www . geesforgeks . org/如何获取 3d numpy 数组的所有 2d 对角线/](https://www.geeksforgeeks.org/how-to-get-all-2d-diagonals-of-a-3d-numpy-array/)

让我们来看看获取三维 NumPy 数组的所有 2D 对角线的程序。所以，为此我们使用了 [**numpy .对角线()**功能的 numpy 库。这个函数从 n 维数组中返回指定的对角线。](https://www.geeksforgeeks.org/python-numpy-matrix-diagonal/)

> **语法:** numpy .对角线(a，axis1，axis 2)
> T3】参数:
> 
> *   **a:** 表示必须从中取对角线的数组
> *   **轴 1:** 代表二维子阵列的第一个轴
> *   **轴 2:** 代表二维子阵列的第二个轴
> 
> **返回:**对角元素的*数组。*

现在，让我们看一个例子:

**例 1:**

## 蟒蛇 3

```py
# Import the numpy package
import numpy as np

# Create 3D-numpy array
# of 4 rows and 4 columns
arr = np.arange(3 * 4 * 4).reshape(3, 4, 4)

print("Original 3d array:\n", 
      arr)

# Create 2D diagonal array
diag_arr = np.diagonal(arr, 
                       axis1 = 1,
                       axis2 = 2)

print("2d diagonal array:\n", 
      diag_arr)
```

**输出:**

```py
Original 3d array:
 [[[ 0  1  2  3]
  [ 4  5  6  7]
  [ 8  9 10 11]
  [12 13 14 15]]

 [[16 17 18 19]
  [20 21 22 23]
  [24 25 26 27]
  [28 29 30 31]]

 [[32 33 34 35]
  [36 37 38 39]
  [40 41 42 43]
  [44 45 46 47]]]
2d diagonal array:
 [[ 0  5 10 15]
 [16 21 26 31]
 [32 37 42 47]]

```

**例 2:**

## 蟒蛇 3

```py
# Import the numpy package
import numpy as np

# Create 3D numpy array
# of 3 rows and 4 columns
arr = np.arange(3 * 3 * 4).reshape(3, 3, 4)

print("Original 3d array:\n", 
      arr)

# Create 2D diagonal array
diag_arr = np.diagonal(arr, 
                       axis1 = 1,
                       axis2 = 2)

print("2d diagonal array:\n",
      diag_arr)
```

**输出:**

```py
Original 3d array:
 [[[ 0  1  2  3]
  [ 4  5  6  7]
  [ 8  9 10 11]]

 [[12 13 14 15]
  [16 17 18 19]
  [20 21 22 23]]

 [[24 25 26 27]
  [28 29 30 31]
  [32 33 34 35]]]
2d diagonal array:
 [[ 0  5 10]
 [12 17 22]
 [24 29 34]]

```

**例 3:**

## 蟒蛇 3

```py
# Import the numpy package
import numpy as np

# Create 3D numpy array
# of 5 rows and 6 columns
arr = np.arange(3 * 5 * 6).reshape(3, 5, 6)
print("Original 3d array:\n",
      arr)

# Create 2D diagonal array
diag_arr = np.diagonal(arr, 
                       axis1 = 1,
                       axis2 = 2)

print("2d diagonal array:\n",
      diag_arr)
```

**输出:**

```py
Original 3d array:
 [[[ 0  1  2  3  4  5]
  [ 6  7  8  9 10 11]
  [12 13 14 15 16 17]
  [18 19 20 21 22 23]
  [24 25 26 27 28 29]]

 [[30 31 32 33 34 35]
  [36 37 38 39 40 41]
  [42 43 44 45 46 47]
  [48 49 50 51 52 53]
  [54 55 56 57 58 59]]

 [[60 61 62 63 64 65]
  [66 67 68 69 70 71]
  [72 73 74 75 76 77]
  [78 79 80 81 82 83]
  [84 85 86 87 88 89]]]
2d diagonal array:
 [[ 0  7 14 21 28]
 [30 37 44 51 58]
 [60 67 74 81 88]]

```