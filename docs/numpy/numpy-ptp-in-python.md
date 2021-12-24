# python 中的 numpy.ptp()

> 原文:[https://www.geeksforgeeks.org/numpy-ptp-in-python/](https://www.geeksforgeeks.org/numpy-ptp-in-python/)

**numpy.ptp()** 函数通过找出给定数字的范围，在统计中发挥重要作用。范围=最大值–最小值。

> **语法:** ndarray.ptp(arr，axis=None，out=None)
> **参数:**
> **arr :** 输入数组。
> **轴:**轴，我们希望范围值沿着该轴。否则，它将考虑将 arr 展平(在所有轴上工作)。axis = 0 表示沿列工作，axis = 1 表示沿行工作。
> **out:**【n 数组，可选】我们要放置结果的不同数组。数组必须具有与预期输出相同的维度。
> **返回:**数组的范围(如果轴为无，则为标量值)或具有沿指定轴的值范围的数组。

**代码#1:工作**

## 计算机编程语言

```
# Python Program illustrating
# numpy.ptp() method

import numpy as np

# 1D array
arr = [1, 2, 7, 20, np.nan]
print("arr : ", arr)
print("Range of arr : ", np.ptp(arr))

# 1D array
arr = [1, 2, 7, 10, 16]
print("arr : ", arr)
print("Range of arr : ", np.ptp(arr))
```

**输出:**

```
arr :  [1, 2, 7, 20, nan]
Range of arr :  nan
arr :  [1, 2, 7, 10, 16]
Range of arr :  15
```

**代码#2 :**

## 计算机编程语言

```
# Python Program illustrating
# numpy.ptp() method

import numpy as np

# 3D array
arr = [[14, 17, 12, 33, 44], 
       [15, 6, 27, 8, 19],
       [23, 2, 54, 1, 4,]]
print("\narr : \n", arr)

# Range of the flattened array
print("\nRange of arr, axis = None : ", np.ptp(arr))

# Range along the first axis
# axis 0 means vertical
print("Range of arr, axis = 0 : ", np.ptp(arr, axis = 0))

# Range along the second axis
# axis 1 means horizontal
print("Min of arr, axis = 1 : ", np.ptp(arr, axis = 1)) 
```

**输出:**

```
arr : 
 [[14, 17, 12, 33, 44], [15, 6, 27, 8, 19], [23, 2, 54, 1, 4]]

Range of arr, axis = None :  53
Range of arr, axis = 0 :  [ 9 15 42 32 40]
Min of arr, axis = 1 :  [32 21 53]
```

**代码#3 :**

## 计算机编程语言

```
# Python Program illustrating
# numpy.ptp() method

import numpy as np

arr1 = np.arange(5)
print("\nInitial arr1 : ", arr1)

# using out parameter
np.ptp(arr, axis = 0, out = arr1)

print("Changed arr1(having results) : ", arr1)
```

**输出:**

```
Initial arr1 :  [0 1 2 3 4]
Changed arr1(having results) :  [ 9 15 42 32 40]
```