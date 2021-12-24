# Python 中的 numpy.sum()

> 原文:[https://www.geeksforgeeks.org/numpy-sum-in-python/](https://www.geeksforgeeks.org/numpy-sum-in-python/)

**`numpy.sum(arr, axis, dtype, out)` :** 该函数返回指定轴上数组元素的总和。

> **参数:**
> **arr :** 输入阵。
> **轴:**轴，我们要沿着该轴计算和值。否则，它将考虑将 arr 展平(在所有轴上工作)。axis = 0 表示沿列工作，axis = 1 表示沿行工作。
> **出:**不同的数组中我们要放置的结果。数组必须具有与预期输出相同的维度。默认值为无。
> **初始值:**【标量，可选】总和的起始值。
> 
> **返回:**数组元素的总和(如果轴为无，则为标量值)或沿指定轴具有总和值的数组。

**代码#1:**

```py
# Python Program illustrating 
# numpy.sum() method
import numpy as np 

# 1D array 
arr = [20, 2, .2, 10, 4]  

print("\nSum of arr : ", np.sum(arr)) 

print("Sum of arr(uint8) : ", np.sum(arr, dtype = np.uint8)) 
print("Sum of arr(float32) : ", np.sum(arr, dtype = np.float32))

print ("\nIs np.sum(arr).dtype == np.uint : ", 
       np.sum(arr).dtype == np.uint) 

print ("Is np.sum(arr).dtype == np.float : ", 
       np.sum(arr).dtype == np.float) 
```

**输出:**

```py
Sum of arr :  36.2
Sum of arr(uint8) :  36
Sum of arr(float32) :  36.2

Is np.sum(arr).dtype == np.uint :  False
Is np.sum(arr).dtype == np.uint :  True

```

**代码#2:**

```py
# Python Program illustrating 
# numpy.sum() method
import numpy as np 

# 2D array 
arr = [[14, 17, 12, 33, 44],   
       [15, 6, 27, 8, 19],  
       [23, 2, 54, 1, 4,]]  

print("\nSum of arr : ", np.sum(arr)) 

print("Sum of arr(uint8) : ", np.sum(arr, dtype = np.uint8)) 
print("Sum of arr(float32) : ", np.sum(arr, dtype = np.float32))

print ("\nIs np.sum(arr).dtype == np.uint : ", 
                 np.sum(arr).dtype == np.uint) 

print ("Is np.sum(arr).dtype == np.uint : ", 
              np.sum(arr).dtype == np.float) 
```

**输出:**

```py
Sum of arr :  279
Sum of arr(uint8) :  23
Sum of arr(float32) :  279.0

Is np.sum(arr).dtype == np.uint :  False
Is np.sum(arr).dtype == np.uint :  False

```

**代码#3:**

```py
# Python Program illustrating 
# numpy.sum() method 

import numpy as np 

# 2D array  
arr = [[14, 17, 12, 33, 44],   
       [15, 6, 27, 8, 19],  
       [23, 2, 54, 1, 4,]]  

print("\nSum of arr : ", np.sum(arr)) 
print("Sum of arr(axis = 0) : ", np.sum(arr, axis = 0)) 
print("Sum of arr(axis = 1) : ", np.sum(arr, axis = 1))

print("\nSum of arr (keepdimension is True): \n",
      np.sum(arr, axis = 1, keepdims = True))
```

**输出:**

```py
Sum of arr :  279
Sum of arr(axis = 0) :  [52 25 93 42 67]
Sum of arr(axis = 1) :  [120  75  84]

Sum of arr (keepdimension is True): 
 [[120]
 [ 75]
 [ 84]]
```