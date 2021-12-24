# python 中的 numpy.nanmin()

> 原文:[https://www.geeksforgeeks.org/numpy-nanmin-in-python/](https://www.geeksforgeeks.org/numpy-nanmin-in-python/)

**`numpy.nanmin()`** 函数用于当要返回一个数组的最小值或沿该数组的任何特定提到的轴时，忽略任何 Nan 值。

> **语法:** numpy.nanmin(arr，axis=None，out=None)
> **参数:**
> **arr :** 输入数组。
> **轴:**轴，我们要沿着它取最小值。否则，它将考虑将 arr 展平(在所有轴上工作)。轴= 0 表示沿列
> 工作，轴= 1 表示沿行工作。
> **出:**我们想要放置结果的不同数组。数组必须具有与预期输出相同的维度。
> 
> **返回:**最小数组值(如果轴为无，则为标量值)或沿指定轴具有最小值的数组。

**代码#1:工作**

```py
# Python Program illustrating 
# numpy.nanmin() method 

import numpy as np

# 1D array 
arr = [1, 2, 7, 0, np.nan]
print("arr : ", arr) 
print("Min of arr : ", np.amin(arr))

# nanmin ignores NaN values. 
print("nanMin of arr : ", np.nanmin(arr))
```

**输出:**

```py
arr :  [1, 2, 7, 0, nan]
Min of arr :  nan
nanMin of arr :  0.0

```

**代码#2 :**

```py
# Python Program illustrating 
# numpy.nanmin() method 

import numpy as np

# 2D array 
arr = [[np.nan, 17, 12, 33, 44],  
       [15, 6, 27, 8, 19]] 
print("\narr : \n", arr) 

# Minimum of the flattened array 
print("\nMin of arr, axis = None : ", np.nanmin(arr)) 

# Minimum along the first axis 
# axis 0 means vertical 
print("Min of arr, axis = 0 : ", np.nanmin(arr, axis = 0)) 

# Minimum along the second axis 
# axis 1 means horizontal 
print("Min of arr, axis = 1 : ", np.nanmin(arr, axis = 1))  
```

**输出:**

```py
arr : 
 [[14, 17, 12, 33, 44], [15, 6, 27, 8, 19]]

Min of arr, axis = None :  6
Min of arr, axis = 0 :  [14  6 12  8 19]
Min of arr, axis = 1 :  [12  6]

```

**代码#3 :**

```py
# Python Program illustrating 
# numpy.nanmin() method 

import numpy as np

arr1 = np.arange(5) 
print("Initial arr1 : ", arr1)

# using out parameter
np.nanmin(arr, axis = 0, out = arr1)

print("Changed arr1(having results) : ", arr1)
```

**输出:**

```py
Initial arr1 :  [0 1 2 3 4]
Changed arr1(having results) :  [14  6 12  8 19]

```