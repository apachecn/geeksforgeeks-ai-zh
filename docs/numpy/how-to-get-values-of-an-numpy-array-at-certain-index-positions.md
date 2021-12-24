# 如何获取 NumPy 数组在特定索引位置的值？

> 原文:[https://www . geeksforgeeks . org/如何在特定索引位置获取数组值/](https://www.geeksforgeeks.org/how-to-get-values-of-an-numpy-array-at-certain-index-positions/)

有时我们需要从源 Numpy 数组中移除值，并在目标数组的特定索引处添加它们。在 NumPy 中，我们有这种灵活性，我们可以从一个数组中移除值，并将它们添加到另一个数组中。我们可以使用 **numpy.put()** 函数来执行这个操作，它可以应用于所有形式的数组，如一维、二维等。

**例 1:**

## 蟒 3

```
# Importing Numpy module
import numpy as np

# Creating 1-D Numpy array
a1 = np.array([11, 10, 22, 30, 33])
print("Array 1 :")
print(a1)

a2 = np.array([1, 15, 60])
print("Array 2 :")
print(a2)

print("\nTake 1 and 15 from Array 2 and put them in\
1st and 5th position of Array 1")

a1.put([0, 4], a2)

print("Resultant Array :")
print(a1)
```