# 生成两个 NumPy 数组的矩阵乘积

> 原文:[https://www . geeksforgeeks . org/generate-a-matrix-product-of-two-numpy-arrays/](https://www.geeksforgeeks.org/generate-a-matrix-product-of-two-numpy-arrays/)

我们可以用函数 np.matmul(a，b)乘两个矩阵。当我们将两个(m*n)和(p*q)阶的数组相乘以得到矩阵乘积时，它的输出包含 m 行和 q 列，其中 n 是 n==p 是一个必要条件。

> **语法:** numpy.matmul( *x1* 、 *x2* 、 */* 、 *out=None* 、 *** 、 *casting='same_kind'* 、 *order='K'* 、 *dtype=None* 、 *subok=True* 【、*签名【T21*

要相乘两个矩阵，取第一个数组的行和第二个数组的列，并相乘相应的元素。然后加上最终答案的值。假设有两个矩阵 A 和 b。

```
A = [[A00, A01],
     [A10, A11]]

B = [[B00, B01],
     [B10, B11]]

Then the product is calculated as shown below
A*B = [[(A00*B00 + A01*B10), (A00*B01 + A01*B11)],
       [(A10*B00 + A11+B10), (A10*B01 + A11*B11)]]

```

下面是实现。

## 蟒蛇 3

```
# Importing Library
import numpy as np

# Finding the matrix product
arr1 = np.array([[1, 2, 3], [4, 5, 6],
                 [7, 8, 9]])
arr2 = np.array([[11, 12, 13], [14, 15, 16],
                 [17, 18, 19]])

matrix_product = np.matmul(arr1, arr2)
print("Matrix Product is ")
print(matrix_product)
print()

arr1 = np.array([[2,2],[3,3]])
arr2 = np.array([[1,2,3],[4,5,6]])

matrix_product = np.matmul(arr1, arr2)
print("Matrix Product is ")
print(matrix_product)
print()

arr1 = np.array([[100,200],[300,400]])
arr2 = np.array([[1,2],[4,6]])

matrix_product = np.matmul(arr1, arr2)
print("Matrix Product is ")
print(matrix_product)
```

**输出:**

```
Matrix Product is 
[[ 90  96 102]
 [216 231 246]
 [342 366 390]]

Matrix Product is 
[[10 14 18]
 [15 21 27]]

Matrix Product is 
[[ 900 1400]
 [1900 3000]]

```