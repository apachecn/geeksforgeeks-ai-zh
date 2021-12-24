# 计算 2D NumPy 数组中所有列的总和

> 原文:[https://www . geeksforgeeks . org/计算 2d numpy 数组中所有列的总和/](https://www.geeksforgeeks.org/calculate-the-sum-of-all-columns-in-a-2d-numpy-array/)

让我们看看如何计算 2D NumPy 数组中所有列的总和。
**方法 1 :** 使用嵌套循环按列访问数组元素，然后将它们的和存储在变量中，然后打印出来。
**例 1:**

## 蟒蛇 3

```py
# importing required libraries
import numpy

# explicit function to compute column wise sum
def colsum(arr, n, m):
    for i in range(n):
        su = 0;
        for j in range(m):
            su += arr[j][i]
        print(su, end = " ")   

# creating the 2D Array
TwoDList = [[1, 2, 3], [4, 5, 6],
            [7, 8, 9], [10, 11, 12]]
TwoDArray = numpy.array(TwoDList)

# displaying the 2D Array
print("2D Array:")
print(TwoDArray)

# printing the sum of each column
print("\nColumn-wise Sum:")
colsum(TwoDArray, len(TwoDArray[0]), len(TwoDArray))
```

**输出:**

```py
2D Array:
[[ 1  2  3]
 [ 4  5  6]
 [ 7  8  9]
 [10 11 12]]

Column-wise Sum:
22 26 30 
```

**例 2 :**

## 蟒蛇 3

```py
# importing required libraries
import numpy

# explicit function to compute column wise sum
def colsum(arr, n, m):
    for i in range(n):
        su = 0;
        for j in range(m):
            su += arr[j][i]
        print(su, end = " ")   

# creating the 2D Array
TwoDList = [[1.2, 2.3], [3.4, 4.5]]
TwoDArray = numpy.array(TwoDList)

# displaying the 2D Array
print("2D Array:")
print(TwoDArray)

# printing the sum of each column
print("\nColumn-wise Sum:")
colsum(TwoDArray, len(TwoDArray[0]), len(TwoDArray))
```

**输出:**

```py
2D Array:
[[1.2 2.3]
 [3.4 4.5]]

Column-wise Sum:
4.6 6.8 
```

**方法 2:** 使用 NumPy，numpy.sum(arr，axis，dtype，out)函数中的 **sum()** 函数返回指定轴上数组元素的和。要计算所有列的总和，sum()函数中的 axis 参数应为 0。
**例 1 :**

## 蟒蛇 3

```py
# importing required libraries
import numpy

# creating the 2D Array
TwoDList = [[1, 2, 3], [4, 5, 6],
            [7, 8, 9], [10, 11, 12]]
TwoDArray = numpy.array(TwoDList)

# displaying the 2D Array
print("2D Array:")
print(TwoDArray)

# printing the sum of each column
print("\nColumn-wise Sum:")
print(numpy.sum(TwoDArray, axis = 0))
```

**输出:**

```py
2D Array:
[[ 1  2  3]
 [ 4  5  6]
 [ 7  8  9]
 [10 11 12]]

Column-wise Sum:
22 26 30
```

**例 2 :**

## 蟒蛇 3

```py
# importing required libraries
import numpy

# creating the 2D Array
TwoDList =[[1.2, 2.3], [3.4, 4.5]]
TwoDArray = numpy.array(TwoDList)

# displaying the 2D Array
print("2D Array:")
print(TwoDArray)

# printing the sum of each column
print("\nColumn-wise Sum:")
print(*numpy.sum(TwoDArray, axis = 0))
```

**输出:**

```py
2D Array:
[[1.2 2.3]
 [3.4 4.5]]

Column-wise Sum:
4.6 6.8
```