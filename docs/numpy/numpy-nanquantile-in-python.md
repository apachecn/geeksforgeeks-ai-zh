# python 中的 num py . nanquantile()

> 原文:[https://www.geeksforgeeks.org/numpy-nanquantile-in-python/](https://www.geeksforgeeks.org/numpy-nanquantile-in-python/)

**`numpy.nanquantile(arr, q, axis = None)` :** 沿指定轴计算给定数据(数组元素)的第 q <sup>个</sup>分位数，忽略 nan 值。

当处理正态分布时，分位数在统计学中起着非常重要的作用。
![](img/a50f8c8714504ca52b2a4a8fab283e59.png)
在上图中，`Q2`是正态分布数据的`median`。`Q3 - Q2`表示给定数据集的**分位数区间**。

> **参数:**
> **arr:**【array _ like】输入数组。
> **q :** 分位数值。
> **轴:**【int 或 int 的元组】轴，我们要沿着该轴计算分位数值。否则，它将考虑将 arr 展平(在所有轴上工作)。axis = 0 表示沿列工作，axis = 1 表示沿行工作。
> **out:**【n 数组，可选】我们要放置结果的不同数组。数组必须具有与预期输出相同的维度。
> 
> **结果:** q <sup>第</sup>个数组分位数(如果轴为无，则为标量值)或沿指定轴有分位数值的数组，忽略 nan 值。

**代码#1 :**

```py
# Python Program illustrating 
# numpy.nanquantile() method  
import numpy as np 

# 1D array 
arr = [20, 2, 7, np.nan, 34] 
print("arr : ", arr) 

print("\n-Q1 quantile of arr : ", np.quantile(arr, .50)) 
print("Q2 - quantile of arr : ", np.quantile(arr, .25)) 
print("Q3 - quantile of arr : ", np.quantile(arr, .75)) 

print("\nQ1 - nanquantile of arr : ", np.nanquantile(arr, .50)) 
print("Q2 - nanquantile of arr : ", np.nanquantile(arr, .25)) 
print("Q3 - nanquantile of arr : ", np.nanquantile(arr, .75)) 
```

**输出:**

```py
arr : [20, 2, 7, nan, 34]

Q1 - quantile of arr : nan
Q2 - quantile of arr : nan
Q3 - quantile of arr : nan

Q1 - nanquantile of arr : 13.5
Q2 - nanquantile of arr : 5.75
Q3 - nanquantile of arr : 23.5

```

**代码#2:**

```py
# Python Program illustrating 
# numpy.nanquantile() method 

import numpy as np 

# 2D array 
arr = [[14, np.nan, 12, 33, 44], 
       [15, np.nan, 27, 8, 19], 
       [23, 2, np.nan, 1, 4, ]] 
print("\narr : \n", arr) 

# quantile of the flattened array 
print("\nQ2 quantile of arr, axis = None : ", np.quantile(arr, .50)) 
print("\nQ2 quantile of arr, axis = None : ", np.nanquantile(arr, .50)) 
print("0th quantile of arr, axis = None : ", np.nanquantile(arr, 0)) 
```

**输出:**

```py
arr : 
[[14, nan, 12, 33, 44], [15, nan, 27, 8, 19], [23, 2, nan, 1, 4]]

Q2 quantile of arr, axis = None : nan
Q2 quantile of arr, axis = None : 14.5
0th quantile of arr, axis = None : 1.0

```

**代码#3:**

```py
# Python Program illustrating 
# numpy.nanquantile() method 
import numpy as np 

# 2D array 
arr = [[14, np.nan, 12, 33, 44], 
    [15, np.nan, 27, 8, 19], 
    [23, 2, np.nan, 1, 4, ]] 
print("\narr : \n", arr) 

# quantile along the axis = 0 
print("\nQ2 quantile of arr, axis = 0 : ", np.nanquantile(arr, .50, axis = 0)) 
print("0th quantile of arr, axis = 0 : ", np.nanquantile(arr, 0, axis = 0)) 

# quantile along the axis = 1 
print("\nQ2 quantile of arr, axis = 1 : ", np.nanquantile(arr, .50, axis = 1)) 
print("0th quantile of arr, axis = 1 : ", np.nanquantile(arr, 0, axis = 1)) 

print("\nQ2 quantile of arr, axis = 1 : \n",
  np.nanquantile(arr, .50, axis = 1, keepdims = True)) 
print("\n0th quantile of arr, axis = 1 : \n",
    np.nanquantile(arr, 0, axis = 1, keepdims = True)) 
```

**输出:**

```py
arr : 
[[14, nan, 12, 33, 44], [15, nan, 27, 8, 19], [23, 2, nan, 1, 4]]

Q2 quantile of arr, axis = 0 : [15\.  2\. 19.5  8\.  19\. ]
0th quantile of arr, axis = 0 : [14\. 2\. 12\.  1\.  4.]

Q2 quantile of arr, axis = 1 : [23.5 17\.   3\. ]
0th quantile of arr, axis = 1 : [12\.  8\.  1.]

Q2 quantile of arr, axis = 1 : 
[[23.5]
[17\. ]
[ 3\. ]]

0th quantile of arr, axis = 1 : 
[[12.]
[ 8.]
[ 1.]]
```