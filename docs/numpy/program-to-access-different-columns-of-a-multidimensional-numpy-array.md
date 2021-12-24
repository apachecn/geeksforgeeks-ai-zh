# 访问多维 Numpy 数组不同列的程序

> 原文:[https://www . geesforgeks . org/program-to-access-不同列的多维 numpy-array/](https://www.geeksforgeeks.org/program-to-access-different-columns-of-a-multidimensional-numpy-array/)

**先决条件:** [Numpy 模块](https://www.geeksforgeeks.org/python-numpy/)

下面的文章讨论了我们如何访问多维 Numpy 数组的不同列。这里，我们使用切片方法来获得所需的功能。

**示例 1:** (访问 Numpy 数组的第一列和最后一列)

## 蟒蛇 3

```py
# Importing Numpy module
import numpy as np

# Creating a 3x3 Numpy array
arr = np.array([[11, 20, 3], 
                [89, 5, 66], 
                [71, 88, 39]])

print("Given Array :")
print(arr)

# Access the First and Last column of array
res_arr = arr[:,[0,2]]
print("\nAccessed Columns :")
print(res_arr)
```

**输出:**

> 给定数组:
> 
> [[11 20  3]
> 
> [89  5 66]
> 
> [71 88 39]]
> 
> 访问的列:
> 
> [[11  3]
> 
> [89 66]
> 
> [71 39]]

**示例 2:** (访问 Numpy 数组的中间和最后一列)

## 蟒蛇 3

```py
# Importing Numpy module
import numpy as np

# Creating a 4x4 Numpy array
arr = np.array([[1, 20, 3, 1], 
                [40, 5, 66, 7], 
                [70, 88, 9, 11],
               [80, 100, 50, 77]])

print("Given Array :")
print(arr)

# Access the Middle and Last column of array
res_arr = arr[:,[1,3]]
print("\nAccessed Columns :")
print(res_arr)
```

**输出:**

> 给定数组:
> 
> [[  1  20   3   1]
> 
> [ 40   5  66   7]
> 
> [ 70  88   9  11]
> 
> [ 80 100  50  77]]
> 
> 访问的列:
> 
> [[ 20   1]
> 
> [  5   7]
> 
> [ 88  11]
> 
> [100  77]]

**示例 3:** (访问 Numpy 数组的最后两列)

## 蟒蛇 3

```py
# Importing Numpy module
import numpy as np

# Creating a 3d (3X4X4) Numpy array
arr = np.array([[[21, 20, 3, 1], 
                [40, 5, 66, 7], 
                [70, 88, 9, 11],
               [80, 100, 50, 77]],

               [[65, 120, 53, 73], 
                [49, 50, 56, 11], 
                [81, 88, 34, 22],
               [564,56, 76, 99]],

               [[45, 85, 38, 455], 
                [40, 53, 69, 6], 
                [50, 528, 654, 11],
               [54, 87, 78, 77]]])

print("Given Array :")
print(arr)

# Access the Last two columns of array
res_arr = arr[2,:,[2,3]]
print("\nAccessed Columns :")
print(res_arr)
```

**输出:**

> 给定数组:
> 
> [[[ 21  20   3   1]
> 
>  [ 40   5  66   7]
> 
>  [ 70  88   9  11]
> 
>  [ 80 100  50  77]]
> 
> [[ 65 120  53  73]
> 
>  [ 49  50  56  11]
> 
>  [ 81  88  34  22]
> 
>  [564  56  76  99]]
> 
> [[ 45  85  38 455]
> 
>  [ 40  53  69   6]
> 
>  [ 50 528 654  11]
> 
>  [ 54  87  78  77]]]
> 
> 访问的列:
> 
> [[ 38  69 654  78]
> 
> [455   6  11  77]]

**示例 4:** (访问 4D Numpy 数组的第一列)

## 蟒蛇 3

```py
# Importing Numpy module
import numpy as np

# Creating a 4D Numpy array
arr = np.array([
  [
    [
      [1,2],
      [3,4]
    ],
    [
      [5,6],
      [7,8]
    ]
  ],
   [
    [
      [9,10],
      [11,12]
    ],
    [
      [13,14],
      [15,16]
    ]
  ]

])

print("Given Array :")
print(arr)

# Access the First three columns of array
res_arr = arr[0,0,:,[0]]
print("\nAccessed Columns :")
print(res_arr)
```

**输出:**

> 给定数组:
> 
> [[[[ 1  2]
> 
>   [ 3  4]]
> 
>  [[ 5  6]
> 
>   [ 7  8]]]
> 
> [[[ 9 10]
> 
>   [11 12]]
> 
>  [[13 14]
> 
>   [15 16]]]]
> 
> 访问的列:
> 
> [[1 3]]