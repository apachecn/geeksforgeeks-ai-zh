# 如何用 NumPy 得到数组的 n 个最大值？

> 原文:[https://www . geeksforgeeks . org/如何使用 numpy 获取数组的 n 个最大值/](https://www.geeksforgeeks.org/how-to-get-the-n-largest-values-of-an-array-using-numpy/)

让我们看看如何使用 NumPy 库获取数组的 n 个最大值的程序。为了从 numpy 数组中获得 n 个最大的值，我们必须首先使用 NumPy 的 [**numpy.argsort()**](https://www.geeksforgeeks.org/numpy-argsort-in-python/) 函数对 NumPy 数组进行排序，然后应用带有负索引的切片概念。

> **语法:** numpy.argsort(arr，axis=-1，kind='quicksort '，order=None)
> 
> **返回:**【index _ Array，ndarray】沿指定轴排序的索引数组。如果 arr 是一维的，那么 arr[index_array]返回一个排序后的 arr。

让我们看一个例子:

**示例 1:** 从 NumPy 数组中获取第一大值。

## 蟒蛇 3

```
# import library
import numpy as np

# create numpy 1d-array
arr = np.array([2, 0,  1, 5,
                4, 1, 9])

print("Given array:", arr)

# sort an array in
# ascending order

# np.argsort() return
# array of indices for
# sorted array
sorted_index_array = np.argsort(arr)

# sorted array
sorted_array = arr[sorted_index_array]

print("Sorted array:", sorted_array)

# we want 1 largest value
n = 1

# we are using negative
# indexing concept

# take n largest value
rslt = sorted_array[-n : ]

# show the output
print("{} largest value:".format(n),
      rslt[0])
```

**输出:**

```
Given array: [2 0 1 5 4 1 9]
Sorted array: [0 1 1 2 4 5 9]
1 largest value: 9

```

**示例 2:** 从 NumPy 数组中获取 3 个最大值。

## 蟒蛇 3

```
# import library
import numpy as np

# create numpy 1d-array
arr = np.array([2, 0,  1, 5,
                4, 1, 9])

print("Given array:", arr)

# sort an array in
# ascending order

# np.argsort() return
# array of indices for
# sorted array
sorted_index_array = np.argsort(arr)

# sorted array
sorted_array = arr[sorted_index_array]

print("Sorted array:", sorted_array)

# we want 3 largest value
n = 3

# we are using negative
# indexing concept

# find n largest value
rslt = sorted_array[-n : ]

# show the output
print("{} largest value:".format(n),
      rslt)
```

**输出:**

```
Given array: [2 0 1 5 4 1 9]
Sorted array: [0 1 1 2 4 5 9]
3 largest value: [4 5 9]

```