# Python 中的 numpy.median()

> 原文:[https://www.geeksforgeeks.org/numpy-median-in-python/](https://www.geeksforgeeks.org/numpy-median-in-python/)

**`numpy.median(arr, axis = None)` :** 计算给定数据(数组元素)沿指定轴的中位数。

**如何计算中位数？**

*   给定数据点。
*   按升序排列
*   如果总项数为奇数，则中位数=中期。
*   中值=中间术语的平均值(如果术语总数为偶数)

> **参数:**
> **arr:**【array _ like】输入数组。
> **轴:**【int 或 int 的元组】轴，我们要沿着该轴计算中位数。否则，它将考虑将 arr 展平(在所有轴上工作)。axis = 0 表示沿列工作，axis = 1 表示沿行工作。
> **出:**【n 数组，可选】我们想要放置结果的不同数组。数组必须具有与预期输出相同的维度。
> **数据类型:**【数据类型，可选】计算中位数时我们想要的类型。
> 
> **结果:**数组的中值(如果轴为无，则为标量值)或沿指定轴具有中值的数组。

**代码#1:**

```py
# Python Program illustrating 
# numpy.median() method 

import numpy as np

# 1D array 
arr = [20, 2, 7, 1, 34]

print("arr : ", arr) 
print("median of arr : ", np.median(arr))

```

**输出:**

```py
arr :  [20, 2, 7, 1, 34]
median of arr :  7.0

```

**代码#2:**

```py
# Python Program illustrating 
# numpy.median() method  
import numpy as np

# 2D array 
arr = [[14, 17, 12, 33, 44],  
       [15, 6, 27, 8, 19], 
       [23, 2, 54, 1, 4, ]] 

# median of the flattened array 
print("\nmedian of arr, axis = None : ", np.median(arr)) 

# median along the axis = 0 
print("\nmedian of arr, axis = 0 : ", np.median(arr, axis = 0)) 

# median along the axis = 1 
print("\nmedian of arr, axis = 1 : ", np.median(arr, axis = 1))

out_arr = np.arange(3)
print("\nout_arr : ", out_arr) 
print("median of arr, axis = 1 : ", 
      np.median(arr, axis = 1, out = out_arr))
```

**输出:**

```py
median of arr, axis = None :  15.0

median of arr, axis = 0 :  [15\.  6\. 27\.  8\. 19.]

median of arr, axis = 1 :  [17\. 15\.  4.]

out_arr :  [0 1 2]
median of arr, axis = 1 :  [17 15  4]

```