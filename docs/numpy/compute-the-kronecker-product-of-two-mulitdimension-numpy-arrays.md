# 计算两个多维 NumPy 阵列的 Kronecker 积

> 原文:[https://www . geeksforgeeks . org/compute-the-kronecker-product-of-two-multi dimension-numpy-arrays/](https://www.geeksforgeeks.org/compute-the-kronecker-product-of-two-mulitdimension-numpy-arrays/)

给定一个 m×n 矩阵 a 和一个 p×q 矩阵 b，它们的 Kronecker 积是一个⊗ B，也叫它们的矩阵直积，是一个(m*p) X (n*q)矩阵。

```
A = | (a00)  (a01) |
    | (a10)  (a11) |

B = | (b00)  (b01) |
    | (b10)  (b11) |

A ⊗ B = | (a00)*(b00)  (a00)*(b01)  (a01)*(b00)  (a01)*(b00) |
        | (a00)*(b01)  (a00)*(b11)  (a01)*(b01)  (a01)*(b11) | 
        | (a10)*(b00)  (a10)*(b01)  (a11)*(b00)  (a11)*(b01) |
        | (a10)*(b10)  (a10)*(b11)  (a11)*(b10)  (a11)*(b11) |
```

可以使用 NumPy 模块中的 [kron()](https://www.geeksforgeeks.org/python-numpy-np-kron-method/) 方法计算两个给定多维数组的 Kronecker 积。kron()方法将两个数组作为参数，并返回这两个数组的 Kronecker 积。

**语法:**

```
numpy.kron(array1, array2)
```

下面是一些程序，描述了 kron()方法在计算两个数组的 Kronecker 积时的实现:

**例 1:**

## 蟒 3

```
# Importing required modules
import numpy

# Creating arrays
array1 = numpy.array([[1, 2], [3, 4]])
print('Array1:\n', array1)

array2 = numpy.array([[5, 6], [7, 8]])
print('\nArray2:\n', array2)

# Computing the Kronecker Product
kroneckerProduct = numpy.kron(array1, array2)
print('\nArray1 ⊗ Array2:')
print(kroneckerProduct)
```

**输出:**

```
Array1:
 [[1 2]
 [3 4]]

Array2:
 [[5 6]
 [7 8]]

Array1 ⊗ Array2:
[[ 5  6 10 12]
 [ 7  8 14 16]
 [15 18 20 24]
 [21 24 28 32]]
```

**例 2:**

## 蟒 3

```
# Importing required modules
import numpy

# Creating arrays
array1 = numpy.array([[1, 2, 3]])
print('Array1:\n', array1)

array2 = numpy.array([[3, 2, 1]])
print('\nArray2:\n', array2)

# Computing the Kronecker Product
kroneckerProduct = numpy.kron(array1, array2)
print('\nArray1 ⊗ Array2:')
print(kroneckerProduct)
```

**输出:**

```
Array1:
 [[1 2 3]]

Array2:
 [[3 2 1]]

Array1 ⊗ Array2:
[[3 2 1 6 4 2 9 6 3]]
```

**例 3:**

## 蟒 3

```
# Importing required modules
import numpy

# Creating arrays
array1 = numpy.array([[1, 2, 3], [4, 5, 6]])
print('Array1:\n', array1)

array2 = numpy.array([[1, 2], [3, 4], [5, 6]])
print('\nArray2:\n', array2)

# Computing the Kronecker Product
kroneckerProduct = numpy.kron(array1, array2)
print('\nArray1 ⊗ Array2:')
print(kroneckerProduct)
```

**输出:**

```
Array1:
 [[1 2 3]
 [4 5 6]]

Array2:
 [[1 2]
 [3 4]
 [5 6]]

Array1 ⊗ Array2:
[[ 1  2  2  4  3  6]
 [ 3  4  6  8  9 12]
 [ 5  6 10 12 15 18]
 [ 4  8  5 10  6 12]
```