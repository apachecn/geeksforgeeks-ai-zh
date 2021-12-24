# python 中的 numpy.nanpercentile()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-nanpercentile-in-python/

**`numpy.nanpercentile()`** 函数用于计算沿指定轴的给定数据(数组元素)的第 n 个百分位，并忽略 nan 值。

> **语法:**numpy . nanpercent(arr，q，axis=None，out=None)
> **参数:**
> **arr :** 输入数组。
> **q :** 百分位值。
> **轴:**轴，我们要沿着该轴计算百分位值。否则，它将考虑将 arr 展平(在所有轴上工作)。轴= 0
> 表示沿列工作，轴= 1 表示沿行工作。
> **出:**我们想要放置结果的不同数组。数组必须具有与预期输出相同的维度。
> 
> **返回:**数组的百分位数(如果轴为无，则为标量值)或具有沿指定轴的值的百分位数的数组。

**代码#1:工作**

```py
# Python Program illustrating 
# numpy.nanpercentile() method 

import numpy as np

# 1D array 
arr = [20, 2, 7, np.nan, 34]
print("arr : ", arr) 
print("30th percentile of arr : ",
       np.percentile(arr, 50))
print("25th percentile of arr : ",
       np.percentile(arr, 25))
print("75th percentile of arr : ",
       np.percentile(arr, 75))

print("\n30th percentile of arr : ",
      np.nanpercentile(arr, 50))
print("25th percentile of arr : ",
       np.nanpercentile(arr, 25))
print("75th percentile of arr : ", 
      np.nanpercentile(arr, 75))
```

**输出:**

```py
arr :  [20, 2, 7, nan, 34]
30th percentile of arr :  nan
25th percentile of arr :  nan
75th percentile of arr :  nan

30th percentile of arr :  13.5
25th percentile of arr :  5.75
75th percentile of arr :  23.5

```

**代码#2 :**

```py
# Python Program illustrating 
# numpy.nanpercentile() method 

import numpy as np

# 2D array 
arr = [[14, np.nan, 12, 33, 44],  
       [15, np.nan, 27, 8, 19], 
       [23, 2, np.nan, 1, 4,]] 
print("\narr : \n", arr) 

# Percentile of the flattened array 
print("\n50th Percentile of arr, axis = None : ", 
      np.percentile(arr, 50)) 
print("\n50th Percentile of arr, axis = None : ", 
      np.nanpercentile(arr, 50)) 
print("0th Percentile of arr, axis = None : ", 
      np.nanpercentile(arr, 0)) 

# Percentile along the axis = 0 
print("\n50th Percentile of arr, axis = 0 : ", 
      np.nanpercentile(arr, 50, axis =0)) 
print("0th Percentile of arr, axis = 0 : ", 
      np.nanpercentile(arr, 0, axis =0)) 

# Percentile along the axis = 1 
print("\n50th Percentile of arr, axis = 1 : ", 
      np.nanpercentile(arr, 50, axis =1)) 
print("0th Percentile of arr, axis = 1 : ", 
      np.nanpercentile(arr, 0, axis =1)) 

print("\n0th Percentile of arr, axis = 1 : \n", 
      np.nanpercentile(arr, 50, axis =1, keepdims=True))
print("\n0th Percentile of arr, axis = 1 : \n", 
      np.nanpercentile(arr, 0, axis =1, keepdims=True))

```

**输出:**

```py
arr : 
 [[14, nan, 12, 33, 44], [15, nan, 27, 8, 19], [23, 2, nan, 1, 4]]

50th Percentile of arr, axis = None :  nan

50th Percentile of arr, axis = None :  14.5
0th Percentile of arr, axis = None :  1.0

50th Percentile of arr, axis = 0 :  [15\.   2\.  19.5  8\.  19\. ]
0th Percentile of arr, axis = 0 :  [14\.  2\. 12\.  1\.  4.]

50th Percentile of arr, axis = 1 :  [23.5 17\.   3\. ]
0th Percentile of arr, axis = 1 :  [12\.  8\.  1.]

0th Percentile of arr, axis = 1 : 
 [[23.5]
 [17\. ]
 [ 3\. ]]

0th Percentile of arr, axis = 1 : 
 [[12.]
 [ 8.]
 [ 1.]]

```

**代码#3 :**

```py
# Python Program illustrating 
# numpy.nanpercentile() method 

import numpy as np

 # 2D array 
arr = [[14, np.nan, 12, 33, 44],  
       [15, np.nan, 27, 8, 19], 
       [23, np.nan, np.nan, 1, 4,]] 
print("\narr : \n", arr) 
# Percentile along the axis = 1 
print("\n50th Percentile of arr, axis = 1 : ", 
      np.nanpercentile(arr, 50, axis =1)) 
print("\n50th Percentile of arr, axis = 0 : ", 
      np.nanpercentile(arr, 50, axis =0)) 
```

**输出:**

```py
arr : 
 [[14, nan, 12, 33, 44], [15, nan, 27, 8, 19], [23, nan, nan, 1, 4]]

50th Percentile of arr, axis = 1 :  [23.5 17\.   4\. ]

50th Percentile of arr, axis = 0 :  [15\.   nan 19.5  8\.  19\. ]
RuntimeWarning: All-NaN slice encountered
  overwrite_input, interpolation)

```