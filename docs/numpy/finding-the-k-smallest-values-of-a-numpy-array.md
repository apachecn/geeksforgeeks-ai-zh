# 求 NumPy 数组的 k 个最小值

> 原文:[https://www . geeksforgeeks . org/find-k-a-numpy-array 的最小值/](https://www.geeksforgeeks.org/finding-the-k-smallest-values-of-a-numpy-array/)

在本文中，让我们看看如何从一个 NumPy 数组中找到 k 个最小值。

**示例:**

```
Input: [1,3,5,2,4,6] 
k = 3

Output: [1,2,3] 

```

**方法 1:** 使用 [np.sort()](https://www.geeksforgeeks.org/numpy-sort-in-python/) 。

**进场:**

1.  创建一个 NumPy 数组。
2.  确定 k 的值。
3.  使用 Sort()方法按升序对数组进行排序。
4.  打印排序数组的前 k 个值。

## 蟒蛇 3

```
# importing the modules
import numpy as np

# creating the array 
arr = np.array([23, 12, 1, 3, 4, 5, 6])
print("The Original Array Content")
print(arr)

# value of k
k = 4

# sorting the array
arr1 = np.sort(arr)

# k smallest number of array
print(k, "smallest elements of the array")
print(arr1[:k])
```

**输出:**

```
The Original Array Content
[23 12  1  3  4  5  6]
4 smallest elements of the array
[1 3 4 5]

```

**方法二:**使用 [np.argpartition()](https://www.geeksforgeeks.org/numpy-argpartition-in-python/)

**进场:**

1.  创建一个 NumPy 数组。
2.  确定 k 的值。
3.  使用 argpartition()方法获取最小 k 个元素的索引。
4.  从从 argpartition()获得的数组中获取前 k 个值，并打印它们相对于原始数组的索引值。

## 蟒蛇 3

```
# importing the module
import numpy as np

# creating the array 
arr = np.array([23, 12, 1, 3, 4, 5, 6])
print("The Original Array Content")
print(arr)

# value of k
k = 4

# using np.argpartition()
result = np.argpartition(arr, k)

# k smallest number of array
print(k, "smallest elements of the array")
print(arr[result[:k]])
```

**输出:**

```
The Original Array Content
[23 12  1  3  4  5  6]
4 smallest elements of the array
[4 3 1 5]

```