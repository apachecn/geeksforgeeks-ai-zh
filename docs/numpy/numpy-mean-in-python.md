# Python 中的 numpy.mean()

> 原文:[https://www.geeksforgeeks.org/numpy-mean-in-python/](https://www.geeksforgeeks.org/numpy-mean-in-python/)

**`numpy.mean(arr, axis = None)` :** 计算给定数据(数组元素)沿指定轴的算术平均值(平均值)。

> **参数:**
> **arr:**【array _ like】输入数组。
> **轴:**【int 或 int 的元组】轴，我们要沿着该轴计算算术平均值。否则，将考虑将 arr 展平(在所有
> 轴上工作)。axis = 0 表示沿列工作，axis = 1 表示沿行工作。
> **out:**【n 数组，可选】我们要放置结果的不同数组。数组必须具有与预期输出相同的维度。
> **数据类型:**【数据类型，可选】计算平均值时我们想要的类型。
> 
> **结果:**数组(如果轴为无，则为标量值)或沿指定轴具有平均值的数组的算术平均值。

**代码#1:**

```
# Python Program illustrating 
# numpy.mean() method 
import numpy as np

# 1D array 
arr = [20, 2, 7, 1, 34]

print("arr : ", arr) 
print("mean of arr : ", np.mean(arr))

```

**输出:**

```
arr :  [20, 2, 7, 1, 34]
mean of arr :  12.8

```

**代码#2:**

```
# Python Program illustrating 
# numpy.mean() method   
import numpy as np

# 2D array 
arr = [[14, 17, 12, 33, 44],  
       [15, 6, 27, 8, 19], 
       [23, 2, 54, 1, 4, ]] 

# mean of the flattened array 
print("\nmean of arr, axis = None : ", np.mean(arr)) 

# mean along the axis = 0 
print("\nmean of arr, axis = 0 : ", np.mean(arr, axis = 0)) 

# mean along the axis = 1 
print("\nmean of arr, axis = 1 : ", np.mean(arr, axis = 1))

out_arr = np.arange(3)
print("\nout_arr : ", out_arr) 
print("mean of arr, axis = 1 : ", 
      np.mean(arr, axis = 1, out = out_arr))
```

**输出:**

```
mean of arr, axis = None :  18.6

mean of arr, axis = 0 :  [17.33333333  8.33333333 31\.         14\.         22.33333333]

mean of arr, axis = 1 :  [24\.  15\.  16.8]

out_arr :  [0 1 2]
mean of arr, axis = 1 :  [24 15 16]

```