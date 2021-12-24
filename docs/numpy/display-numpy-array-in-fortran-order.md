# 以 Fortran 顺序显示 Numpy 数组

> 原文:[https://www . geeksforgeeks . org/display-numpy-array-in-fortran-order/](https://www.geeksforgeeks.org/display-numpy-array-in-fortran-order/)

Fortran 顺序/数组是一种特殊情况，其中数组的所有元素都以列主顺序存储。有时我们需要以 fortran 顺序显示数组，因为这个 numpy 有一个名为 **numpy.nditer()** 的函数。

> **语法:** numpy.nditer(op，flags=None，op_flags=None，op _ dtypes = None，order='K '，casting='safe '，op_axes=None，itershape=None，buffersize=0)

**例 1:**

## 蟒蛇 3

```py
# importing Numpy package
import numpy as np

# creating a Numpy array
num_array = np.arange(12).reshape(3, 4)

print("Array:")
print(num_array)

# Display array in Fortran order
# using numpy.nditer()
print("\nElements of the array in Fortan array:")
for num_array in np.nditer(num_array, order="F"):
    print(num_array, end=' ')
```

**输出:**

```py
Array:
[[ 0  1  2  3]
[ 4  5  6  7]
[ 8  9 10 11]]

Elements of the array in Fortan array:
0 4 8 1 5 9 2 6 10 3 7 11

```

**例 2:**

## 蟒蛇 3

```py
# importing Numpy package 
import numpy as np

# creating a Numpy array
num_array = np.arange(12).reshape(2, 6)

print("Array:")
print(num_array)

# Display array in Fortran order 
# using numpy.nditer() 
print("\nElements of the array in Fortan array:")
for num_array in np.nditer(num_array, order="F"):
    print(num_array,end=' ')
```

**输出:**

```py
Array:
[[ 0  1  2  3  4  5]
[ 6  7  8  9 10 11]]

Elements of the array in Fortan array:
0 6 1 7 2 8 3 9 4 10 5 11

```

**例 3:**

## 蟒蛇 3

```py
# importing Numpy package 
import numpy as np

# creating a Numpy array
num_array = np.arange(42).reshape(6, 7)

print("Array:")
print(num_array)

# Display array in Fortran order 
# using numpy.nditer() 
print("\nElements of the array in Fortan array:")
for num_array in np.nditer(num_array, order="F"):
    print(num_array,end=' ')
```

**输出:**

> 阵列:
> 【【0 1 2 3 4 5 6】
> 【7 8 9 10 11 12 13】
> 【14 15 16 17 18 19 20】
> 【21 22 23 24 25 26 27】
> 【28 29 30 31 32 33 34】
> 【35 36 37 38 39 40 41】】
> 
> 福坦阵列中的阵列元素:
> 0 7 14 21 28 35 1 8 15 22 29 36 2 9 16 23 30 37 3 10 17 24 31 38 4 11 18 25 32 39 5 12 19 26 33 40 6 13 20 27 34 41