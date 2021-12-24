# 计算 2D 数元阵列中跨维度的平均值

> 原文:[https://www . geeksforgeeks . org/计算二维数组中跨维平均值/](https://www.geeksforgeeks.org/calculate-the-mean-across-dimension-in-a-2d-numpy-array/)

我们可以通过函数 [np.mean()](https://www.geeksforgeeks.org/numpy-mean-in-python/) 使用 numpy 求出 2d 数组的每一行和每一列的平均值。这里我们必须提供寻找平均值的轴。

> **语法:** numpy.mean(arr，axis = None)
> 
> **行平均值:**轴=1
> 
> **列平均值:**轴=0

**示例:**

## 蟒蛇 3

```
# Importing Library
import numpy as np

# creating 2d array
arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Calculating mean across Rows
row_mean = np.mean(arr, axis=1)

row1_mean = row_mean[0]
print("Mean of Row 1 is", row1_mean)

row2_mean = row_mean[1]
print("Mean of Row 2 is", row2_mean)

row3_mean = row_mean[2]
print("Mean of Row 3 is", row3_mean)

# Calculating mean across Columns
column_mean = np.mean(arr, axis=0)

column1_mean = column_mean[0]
print("Mean of column 1 is", column1_mean)

column2_mean = column_mean[1]
print("Mean of column 2 is", column2_mean)

column3_mean = column_mean[2]
print("Mean of column 3 is", column3_mean)
```

输出:

```
Mean of Row 1 is 2.0
Mean of Row 2 is 5.0
Mean of Row 3 is 8.0
Mean of column 1 is 4.0
Mean of column 2 is 5.0
Mean of column 3 is 6.0

```