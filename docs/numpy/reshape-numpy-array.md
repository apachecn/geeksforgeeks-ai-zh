# 数码子数组

> 原文:[https://www.geeksforgeeks.org/reshape-numpy-array/](https://www.geeksforgeeks.org/reshape-numpy-array/)

**NumPy** 是一个通用的数组处理包。它提供了一个高性能的多维数组对象，以及使用这些数组的工具。它是使用 Python 进行科学计算的基本包。Numpy 基本上用于创建 n 维数组。
重塑 numpy 数组简单来说就是改变给定数组的形状，形状基本上告诉了数组的元素个数和维度，通过重塑一个数组我们可以在每个维度上增加或者移除维度或者改变元素个数。
为了重塑 numpy 数组，我们对给定的数组使用重塑方法。

> **语法:**数组.重塑(形状)
> **参数:**它以元组为参数，元组是要形成的新形状
> **返回:**它返回 numpy . ndaray

**注意:**我们也可以使用 NP . resform(array，shape)命令来重塑数组
**重塑:1-D 到 2D**
在这个例子中我们将重塑 1-D 数组的 shape (1，N)到 2-D 数组的 shape (N，M)这里的 M 应该等于 n/N，那里的 N 应该是 N 的因子

## 蟒蛇 3

```py
# importing numpy
import numpy as np

# creating a numpy array
array = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16])

# printing array
print("Array : " + str(array))

# length of array
n = array.size

# N-D array N dimension
N = 4

# calculating M
M = n//N

# reshaping numpy array
# converting it to 2-D from 1-D array
reshaped1 = array.reshape((N, M))

# printing reshaped array
print("First Reshaped Array : ")
print(reshaped1)

# creating another reshaped array
reshaped2 = np.reshape(array, (2, 8))

# printing reshaped array
print("Second Reshaped Array : ")
print(reshaped2)
```

**输出:**

```py
Array : [ 1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16]
First Reshaped Array : 
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]
 [13 14 15 16]]
Second Reshaped Array : 
[[ 1  2  3  4  5  6  7  8]
 [ 9 10 11 12 13 14 15 16]]
```

**重塑:一维到三维**
在这里我们将看到如何将一维数组重塑为三维数组。三维阵列是二维阵列的一维阵列。

## 蟒蛇 3

```py
# importing numpy
import numpy as np

# creating a numpy array
array = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16])

# printing array
print("Array : " + str(array))

# reshaping numpy array
# converting it to 3-D from 1-D array
reshaped = array.reshape((2, 2, 4))

# printing reshaped array
print("Reshaped 3-D Array : ")
print(reshaped)
```

**输出:**

```py
Array : [ 1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16]
Reshaped 3-D Array : 
[[[ 1  2  3  4]
  [ 5  6  7  8]]

 [[ 9 10 11 12]
  [13 14 15 16]]]
```

**重塑 N-D 至 1-D 阵列**
在本例中，我们将看到如何重塑 2-D 或 3-D 阵列以形成 1-D 阵列。我们也可以用重塑(-1)来做到这一点，这里-1 是未知的维度。

## 蟒蛇 3

```py
# importing numpy
import numpy as np

# creating a numpy array
array = np.array([[1, 2, 3],
                 [4, 5, 6],
                 [7, 8, 9]])

# printing array
print(" 2-D Array : ")
print(array)

# reshaping numpy array
# converting it to 1-D from 2-D array
reshaped = array.reshape((9))

# or we can use unknown dimension
# reshaped = array.reshape((-1))

# printing reshaped array
print("Reshaped 1-D Array : ")
print(reshaped)
```

**输出:**

```py
 2-D Array : 
[[1 2 3]
 [4 5 6]
 [7 8 9]]
Reshaped 1-D Array : 
[[1 2 3 4 5 6 7 8 9]]
```

**使用未知维度进行重塑**
我们可以通过使用-1 作为维度之一来重塑一个数组虽然我们不知道所有的新维度，但是我们应该知道所有的其他维度来使用未知维度

## 蟒蛇 3

```py
# importing numpy
import numpy as np

# creating a numpy array
array = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16])

# printing array
print("Array : " + str(array))

# reshaping numpy array
# converting it to 3-D from 1-D array
reshaped1 = array.reshape((2, 2, -1))

# printing reshaped array
print("First Reshaped Array : ")
print(reshaped1)

# converting it to 2-D array
reshaped2 = array.reshape((4, -1))

# printing reshaped array
print("Second Reshaped Array : ")
print(reshaped2)
```

**输出:**

```py
Array : [ 1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16]
First Reshaped Array : 
[[[ 1  2  3  4]
  [ 5  6  7  8]]

 [[ 9 10 11 12]
  [13 14 15 16]]]
Second Reshaped Array : 
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]
 [13 14 15 16]]
```

**在重塑过程中出现错误**
当我们试图将数组重塑为数学上不可能的形状时，就会产生值错误，表示无法重塑数组。例如，当我们试图将具有 4 个元素的 1-D 阵列重塑为维度(3，3)的 2-D 阵列时，这是不可能的，因为新阵列需要 9 个元素

## 蟒蛇 3

```py
# importing numpy
import numpy as np

# creating a numpy array
array = np.array([[1, 2, 3],
                 [4, 5, 6],
                 [7, 8, 9]])

# printing array
print(" 2-D Array : ")
print(array)

# reshaping numpy array
# converting it to 1-D from 2-D array
# rehaping it into 1, 5
reshaped = array.reshape((1, 5))

# or we can use

# printing reshaped array
print("Reshaped 1-D Array : ")
print(reshaped)
```

```py
ValueError: cannot reshape array of size 9 into shape (1, 5)
```