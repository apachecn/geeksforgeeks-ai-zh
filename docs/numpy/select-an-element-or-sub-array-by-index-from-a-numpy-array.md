# 从数值数组中通过索引选择一个元素或子数组

> 原文:[https://www . geeksforgeeks . org/从 numpy 数组中逐个选择元素或子数组/](https://www.geeksforgeeks.org/select-an-element-or-sub-array-by-index-from-a-numpy-array/)

NumPy 数组的元素就像普通数组一样被索引。第一个元素的索引为 0，最后一个元素的索引为 n-1，其中 n 是元素的总数。

## **从 NumPy 数组中选择单个元素**

这些数组中的每个元素都可以使用其索引号来访问。

**示例:**下面的代码显示了如何访问 NumPy 数组的元素。

## 蟒蛇 3

```
import numpy as np

# NumPy Array
numpyArr = np.array([1, 2, 3, 4])
print("numpyArr[0] =", numpyArr[0])
print("numpyArr[-1] =", numpyArr[-1])
```

**输出:**

```
numpyArr[0] = 1
numpyArr[-1] = 4

```

在第一种情况下，我们使用数组的索引号访问数组的第一个元素。在第二种情况下，我们通过使用负索引来访问数组的最后一个元素。

## **从 NumPy 阵列中选择** **子阵列(切片)**

为了得到一个子数组，我们传递一个切片来代替元素索引。

**语法:**

```
numpyArr[x:y]

```

这里 x 和 y 是所需子数组的开始和最后一个索引。

**例:**

## 蟒 3

```
import numpy as np

# NumPy Array
numpyArr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9])

# the slice 3:6 is passed instead 
# of index
print("Sub-Array=", numpyArr[3:6])
```