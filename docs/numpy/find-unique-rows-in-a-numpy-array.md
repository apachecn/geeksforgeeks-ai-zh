# 在 NumPy 数组中查找唯一的行

> 原文:[https://www . geesforgeks . org/find-unique-row-in-a-numpy-array/](https://www.geeksforgeeks.org/find-unique-rows-in-a-numpy-array/)

在本文中，我们将讨论如何在 NumPy 数组中找到唯一的行。为了在 numpy 数组中找到唯一的行，我们使用了 NumPy 库的 [**numpy.unique()**](https://www.geeksforgeeks.org/python-numpy-np-unique-method/) 函数。

> **语法:** numpy.unique(ar，return_index=False，return_inverse=False，return_counts=False，axis=None)

现在，让我们看一个例子:

**例 1:**

## 蟒蛇 3

```
# import library
import numpy as np

# Create a 2D numpy array
arr2D = np.array([[11, 11, 12, 11],
                     [13, 11, 12, 11],
                     [16, 11, 12, 11],
                     [11, 11, 12, 11]])

print('Original Array :' ,
      arr2D, sep = '\n')

# Get unique rows from
# complete 2D-array by 
# passing axis = 0 in 
# unique function along
# with 2D-array
uniqueRows = np.unique(arr2D, 
                       axis = 0)

# print the output result
print('Unique Rows:',
      uniqueRows, sep = '\n')
```

**输出:**

```
Original Array :
[[11 11 12 11]
[13 11 12 11]
[16 11 12 11]
[11 11 12 11]]
Unique Rows:
[[11 11 12 11]
[13 11 12 11]
[16 11 12 11]]

```

**例 2:**

## 蟒蛇 3

```
# import library
import numpy as np

# create 2d numpy array
array = np.array([[1, 2, 3, 4],
                  [3, 2, 4, 1],
                  [6, 8, 1, 2]])

print("Original array: \n",
      array)

# Get unique rows from
# complete 2D-array by 
# passing axis = 0 in 
# unique function along
# with 2D-array
uniqueRows = np.unique(array, 
                       axis = 0)

# print the output result
print('Unique Rows :',
      uniqueRows,
      sep = '\n')
```

**输出:**

```
Original array: 
 [[1 2 3 4]
 [3 2 4 1]
 [6 8 1 2]]
Unique Rows :
[[1 2 3 4]
 [3 2 4 1]
 [6 8 1 2]]

```