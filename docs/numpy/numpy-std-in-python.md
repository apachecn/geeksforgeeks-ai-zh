# Python 中的 numpy.std()

> 原文:[https://www.geeksforgeeks.org/numpy-std-in-python/](https://www.geeksforgeeks.org/numpy-std-in-python/)

**numpy.std(arr，axis = None) :** 计算给定数据(数组元素)沿指定轴(如果有)的标准偏差..

**标准偏差(SD)** 作为给定数据集中数据分布的扩展来测量。
![](img/4a0d323535121aea9e67d9d58ee5e4f7.png)
**举例:**

```
x = 1 1 1 1 1 
Standard Deviation = 0 . 

y = 9, 2, 5, 4, 12, 7, 8, 11, 9, 3, 7, 4, 12, 5, 4, 10, 9, 6, 9, 4 
Step 1 : Mean of distribution 4 = 7
Step 2 : Summation of (x - x.mean())**2 = 178
Step 3 : Finding Mean = 178 /20 = 8.9 
This Result is Variance.
Step 4 : Standard Deviation = sqrt(Variance) = sqrt(8.9) = 2.983..

```

> **参数:**
> **arr:**【array _ like】输入数组。
> **轴:**【int 或 int 的元组】轴，我们要沿着该轴计算标准差。否则，它将考虑将 arr 展平(在所有轴上工作)。轴= 0 表示沿列的标清，轴= 1 表示沿行的标清。
> **出:**【n 数组，可选】我们想要放置结果的不同数组。数组必须具有与预期输出相同的维度。
> **数据类型:**【数据类型，可选】计算 SD 时我们想要的类型。
> 
> **结果:**数组(如果轴为无，则为标量值)或具有沿指定轴的标准偏差值的数组的标准偏差。

**代码#1:**

```
# Python Program illustrating 
# numpy.std() method 
import numpy as np

# 1D array 
arr = [20, 2, 7, 1, 34]

print("arr : ", arr) 
print("std of arr : ", np.std(arr))

print ("\nMore precision with float32")
print("std of arr : ", np.std(arr, dtype = np.float32))

print ("\nMore accuracy with float64")
print("std of arr : ", np.std(arr, dtype = np.float64))
```

**输出:**

```
arr :  [20, 2, 7, 1, 34]
std of arr :  12.576167937809991

More precision with float32
std of arr :  12.576168

More accuracy with float64
std of arr :  12.576167937809991

```

**代码#2:**

```
# Python Program illustrating 
# numpy.std() method 
import numpy as np

# 2D array 
arr = [[2, 2, 2, 2, 2],  
       [15, 6, 27, 8, 2], 
       [23, 2, 54, 1, 2, ], 
       [11, 44, 34, 7, 2]] 

# std of the flattened array 
print("\nstd of arr, axis = None : ", np.std(arr)) 

# std along the axis = 0 
print("\nstd of arr, axis = 0 : ", np.std(arr, axis = 0)) 

# std along the axis = 1 
print("\nstd of arr, axis = 1 : ", np.std(arr, axis = 1))
```

**输出:**

```
std of arr, axis = None :  15.3668474320532

std of arr, axis = 0 :  [ 7.56224173 17.68473918 18.59267329  3.04138127  0\.        ]

std of arr, axis = 1 :  [ 0\.          8.7772433  20.53874388 16.40243884]

```