# 在 NumPy 数组末尾追加值

> 原文:[https://www . geeksforgeeks . org/ending-values-at-of-numpy-array/](https://www.geeksforgeeks.org/appending-values-at-the-end-of-an-numpy-array/)

让我们看看如何在 NumPy 数组的末尾追加值。在数组末尾添加值是一项必要的任务，尤其是当数据不是固定的并且易于更改时。对于这个任务，我们可以使用 [numpy.append()](https://www.geeksforgeeks.org/numpy-append-python/) 。这个函数可以帮助我们在数组的末尾追加一个值和多个值。

> **语法:** numpy.append(数组，值，轴=无)
> **参数:**
> 
> *   **数组:**输入数组。
> *   **值:**要在数组中添加的值。
> *   **轴:**我们要沿其插入值的轴。
> 
> **返回:**数组的一个副本，其值按照所提到的对象
> 沿着给定的轴附加在末尾。

**示例 1:向 1D 数组追加单个值**。对于 1D 数组，使用轴参数是不必要的，因为默认情况下数组是扁平的。

```
# importing the module
import numpy as np

# creating an array
arr = np.array([1, 8, 3, 3, 5])
print('Original Array : ', arr)

# appending to the array
arr = np.append(arr, [7])
print('Array after appending : ', arr)
```

**输出:**

```
Original Array :  [1 8 3 3 5]
Array after appending :  [1 8 3 3 5 7]

```

**例 2 :** 在 1D 数组末尾追加另一个数组。您可以将列表或数组传递给 append 函数，结果将是相同的。

```
# importing the module
import numpy as np

# creating an array
arr1 = np.array([1, 2, 3])
print('First array is : ', arr1)

# creating another array
arr2 = np.array([4, 5, 6])
print('Second array is : ', arr2)

# appending arr2 to arr1
arr = np.append(arr1, arr2)
print('Array after appending : ', arr)
```

**输出:**

```
First array is :  [1 2 3]
Second array is :  [4 5 6]
Array after appending :  [1 2 3 4 5 6]

```

**示例 3 :** 在 n 维数组的末尾追加值。两个数组的维度匹配很重要，否则会产生错误。

```
# importing the module
import numpy as np

# create an array
arr = np.arange(1, 13).reshape(2, 6)
print('Original Array')
print(arr, '\n')

# create another array which is
# to be appended column-wise
col = np.arange(5, 11).reshape(1, 6)
print('Array to be appended column wise')
print(col)
arr_col = np.append(arr, col, axis = 0)
print('Array after appending the values column wise')
print(arr_col, '\n')

# create an array which is
# to be appended row wise
row = np.array([1, 2]).reshape(2, 1)
print('Array to be appended row wise')
print(row)
arr_row = np.append(arr, row, axis = 1)
print('Array after appending the values row wise')
print(arr_row)
```

**输出:**

```
Original Array
[[ 1  2  3  4  5  6]
 [ 7  8  9 10 11 12]] 

Array to be appended column wise
[[ 5  6  7  8  9 10]]
Array after appending the values column wise
[[ 1  2  3  4  5  6]
 [ 7  8  9 10 11 12]
 [ 5  6  7  8  9 10]] 

Array to be appended row wise
[[1]
 [2]]
Array after appending the values row wise
[[ 1  2  3  4  5  6  1]
 [ 7  8  9 10 11 12  2]]

```