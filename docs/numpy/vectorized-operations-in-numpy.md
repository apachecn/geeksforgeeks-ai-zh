# NumPy 中的矢量化运算

> 原文:[https://www . geeksforgeeks . org/矢量化-operations-in-numpy/](https://www.geeksforgeeks.org/vectorized-operations-in-numpy/)

Numpy 数组本质上是同构的，这意味着它是一个只包含单一类型数据的数组。Python 的列表和元组，它们包含的数据类型不受限制。NumPy 上的**矢量化运算**的概念允许在 NumPy 数组对象和数据序列上使用更优化和预编译的函数和数学运算。与简单的非向量化运算相比，输出和运算速度会加快。

**例 1 :** 在 NumPy 数组上使用矢量化求和方法。我们将比较矢量化求和方法和简单的非矢量化操作，即计算 0–14，999 之间数字总和的迭代方法。

## 蟒蛇 3

```py
# importing the modules
import numpy as np
import timeit

# vectorized sum
print(np.sum(np.arange(15000)))

print("Time taken by vectorized sum : ", end = "")
%timeit np.sum(np.arange(15000))

# iterative sum
total = 0
for item in range(0, 15000):
    total += item
a = total
print("\n" + str(a))

print("Time taken by iterative sum : ", end = "")
%timeit a
```