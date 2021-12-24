# 计算 2D NumPy 数组所有列的和

> 原文:[https://www . geeksforgeeks . org/计算 2d numpy 数组所有列的总和/](https://www.geeksforgeeks.org/calculating-the-sum-of-all-columns-of-a-2d-numpy-array/)

让我们看看如何计算二维 NumPy 数组所有列的和。

**示例:**

```
Input : 
[[1, 2, 3, 4, 5],
 [5, 6, 7, 8, 9],
 [2, 1, 5, 7, 8],
 [2, 9, 3, 1, 0]]

Output :  [10, 18, 18, 20, 22]

Input : 
[[5, 4, 1, 7],
 [0, 9, 3, 5], 
 [3, 2, 8, 6]]

Output : [8, 15, 12, 18]

```

**方法 1 :** 我们将使用`[sum()](https://www.geeksforgeeks.org/numpy-sum-in-python/)`方法。我们将通过参数 `axis = 0`逐列获取总和。

```
# importing numpy
import numpy as np

# initialize the 2-d array
arr = np.array([[1, 2, 3, 4, 5],
                [5, 6, 7, 8, 9],
                [2, 1, 5, 7, 8],
                [2, 9, 3, 1, 0]])

# calculating column wise sum
sum_2d = arr.sum(axis = 0)

# displaying the sum
print("Column wise sum is :\n", sum_2d)
```

**输出:**

```
Column wise sum is :
 [10 18 18 20 22]

```

**方法二:**我们也可以使用`**numpy.einsum()**`方法，参数`'ij->j'`。

```
# importing numpy
import numpy as np

# initialize the 2-d array
arr = np.array([[1, 2, 3, 4, 5],
                [5, 6, 7, 8, 9],
                [2, 1, 5, 7, 8],
                [2, 9, 3, 1, 0]])

# calculating column wise sum
sum_2d = np.einsum('ij->j', arr)

# displaying the sum
print("Column wise sum is :\n", sum_2d)
```

**输出:**

```
Column wise sum is :
 [10 18 18 20 22]

```