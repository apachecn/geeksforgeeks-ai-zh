# 在 Python Numpy 中沿多维数组访问数据

> 原文:[https://www . geeksforgeeks . org/access-data-沿-多维-python 中的数组-numpy/](https://www.geeksforgeeks.org/accessing-data-along-multiple-dimensions-arrays-in-python-numpy/)

[NumPy](https://www.geeksforgeeks.org/numpy-in-python-set-1-introduction/)(numeric Python)是一个 Python 库，由多维数组和众多函数组成，用于对数组执行各种数学和逻辑操作。NumPy 还由各种函数组成，用于执行线性代数运算和生成随机数。NumPy 经常与 SciPy 和 Matplotlib 等软件包一起用于技术计算。
n 维(多维)数组具有固定的大小，并且包含相同类型的项目。多维数组的内容可以根据需要通过对数组进行索引和切片来访问和修改。为了访问数组的元素，我们需要首先导入库:

```
import numpy as np
```

我们可以使用**整数索引**来访问数据元素。我们还可以执行**切片**来访问数据的子序列。
**例 1:**

## 蟒蛇 3

```
# 1-dimensional array
array1D = np.array([1, 2, 3, 4, 5])

print(array1D)

# to access elements using positive
# index
print("\nusing positive index :" +str(array1D[0]))
print("using positive index :" +str(array1D[4]))

# negative indexing works in opposite
# direction
print("\nusing negative index :" +str(array1D[-5]))
print("using negative index :" +str(array1D[-1]))
```

**输出:**

```
[1 2 3 4 5]

using positive index :1
using positive index :5

using negative index :5
using negative index :1
```

**例 2:**

## 蟒蛇 3

```
# 2-dimensional array
array2D = np.array([[93,  95],
                    [84, 100],
                    [99,  87]])

print(array2D)
print("shape :" +str(array2D.shape))

print("\npositive indexing :" +str(array2D[1, 0]))
print("negative indexing :" +str(array2D[-2, 0]))

print("\nslicing using positive indices :" +str(array2D[0:3, 1]))
print("slicing using positive indices :" +str(array2D[:, 1]))
print("slicing using negative indices :" +str(array2D[:, -1]))
```

**输出:**

```
[[ 93  95]
 [ 84 100]
 [ 99  87]]
shape :(3, 2)

positive indexing :84
negative indexing :84

slicing using positive indices :[ 95 100  87]
slicing using positive indices :[ 95 100  87]
slicing using negative indices :[ 95 100  87]
```

**例 3:**

## 蟒蛇 3

```
# 3-dimensional array
array3D = np.array([[[ 0,  1,  2],
                     [ 3,  4,  5],
                     [ 6,  7,  8]],

                    [[ 9, 10, 11],
                     [12, 13, 14],
                     [15, 16, 17]],

                    [[18, 19, 20],
                     [21, 22, 23],
                     [24, 25, 26]]])

print(array3D)
print("shape :" +str(array3D.shape))

print("\naccessing element :" +str(array3D[0, 1, 0]))
print("accessing elements of a row and a column of an array:"
      +str(array3D[:, 1, 0]))
print("accessing sub part of an array :" +str(array3D[1]))
```

**输出:**

```
[[[ 0  1  2]
  [ 3  4  5]
  [ 6  7  8]]

 [[ 9 10 11]
  [12 13 14]
  [15 16 17]]

 [[18 19 20]
  [21 22 23]
  [24 25 26]]]
shape :(3, 3, 3)
accessing element :3
accessing elements of a row and a column of an array:[ 3 12 21]
accessing sub part of an array :[[ 9 10 11]
 [12 13 14]
 [15 16 17]]
```