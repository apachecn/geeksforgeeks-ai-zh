# python 中的 numpy.percentile()

> 原文:[https://www.geeksforgeeks.org/numpy-percentile-in-python/](https://www.geeksforgeeks.org/numpy-percentile-in-python/)

**numpy . percent()**函数，用于计算给定数据(数组元素)沿指定轴的第 n 个百分位数。

> **语法:**numpy . percent(arr，n，axis=None，out=None)
> **参数:**
> **arr :** 输入数组。
> **n :** 百分位值。
> **轴:**轴，我们要沿着该轴计算百分位值。否则，它将考虑将 arr 展平(在所有轴上工作)。axis = 0 表示沿列工作，axis = 1 表示沿行工作。
> **出:**我们想要放置结果的不同数组。数组必须具有与预期输出相同的维度。
> **返回:**数组的第 n 个百分位(如果轴为无，则为标量值)或沿指定轴有百分位值的数组。

**代码#1:工作**

## 计算机编程语言

```
# Python Program illustrating
# numpy.percentile() method

import numpy as np

# 1D array
arr = [20, 2, 7, 1, 34]
print("arr : ", arr)
print("50th percentile of arr : ",
       np.percentile(arr, 50))
print("25th percentile of arr : ",
       np.percentile(arr, 25))
print("75th percentile of arr : ",
       np.percentile(arr, 75))
```

**输出:**

```
arr :  [20, 2, 7, 1, 34]
50th percentile of arr :  7.0
25th percentile of arr :  2.0
75th percentile of arr :  20.0

```

**代码#2 :**

## 计算机编程语言

```
# Python Program illustrating
# numpy.percentile() method 

import numpy as np

# 2D array
arr = [[14, 17, 12, 33, 44], 
       [15, 6, 27, 8, 19],
       [23, 2, 54, 1, 4,]]
print("\narr : \n", arr)

# Percentile of the flattened array
print("\n50th Percentile of arr, axis = None : ",
      np.percentile(arr, 50))
print("0th Percentile of arr, axis = None : ",
      np.percentile(arr, 0))

# Percentile along the axis = 0
print("\n50th Percentile of arr, axis = 0 : ",
      np.percentile(arr, 50, axis =0))
print("0th Percentile of arr, axis = 0 : ",
      np.percentile(arr, 0, axis =0))
```

**输出:**

```
arr : 
 [[14, 17, 12, 33, 44], [15, 6, 27, 8, 19], [23, 2, 54, 1, 4]]

50th Percentile of arr, axis = None :  15.0
0th Percentile of arr, axis = None :  1.0

50th Percentile of arr, axis = 0 :  [15\.  6\. 27\.  8\. 19.]
0th Percentile of arr, axis = 0 :  [14\.  2\. 12\.  1\.  4.]

50th Percentile of arr, axis = 1 :  [17\. 15\.  4.]
0th Percentile of arr, axis = 1 :  [12\.  6\.  1.]

```

**代码#3 :**

## 计算机编程语言

```
# Python Program illustrating
# numpy.percentile() method

import numpy as np

# 2D array
arr = [[14, 17, 12, 33, 44], 
       [15, 6, 27, 8, 19],
       [23, 2, 54, 1, 4,]]
print("\narr : \n", arr)

# Percentile along the axis = 1
print("\n50th Percentile of arr, axis = 1 : ",
      np.percentile(arr, 50, axis =1))
print("0th Percentile of arr, axis = 1 : ",
      np.percentile(arr, 0, axis =1))

print("\n0th Percentile of arr, axis = 1 : \n",
      np.percentile(arr, 50, axis =1, keepdims=True))
print("\n0th Percentile of arr, axis = 1 : \n",
      np.percentile(arr, 0, axis =1, keepdims=True))
```

**输出:**

```
arr : 
 [[14, 17, 12, 33, 44], [15, 6, 27, 8, 19], [23, 2, 54, 1, 4]]

0th Percentile of arr, axis = 1 : 
 [[17.]
 [15.]
 [ 4.]]

0th Percentile of arr, axis = 1 : 
 [[12.]
 [ 6.]
 [ 1.]]

```