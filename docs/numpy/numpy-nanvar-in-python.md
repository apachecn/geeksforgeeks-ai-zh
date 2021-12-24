# python 中的 numpy.nanvar()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-nanvar-in-python/

**`numpy.nanvar(arr, axis = None)` :** 计算给定数据(数组元素)沿指定轴(如果有)的方差，同时忽略 NaN 值。
![](img/4a61236bc0b7751e76b76467abd529a2.png)

**示例:**

> x = 1 1 1 1
> 标准差= 0。方差= 0
> 
> y = 9，2，5，4，12，7，8，11，9，3，7，4，12，5，4，10，9，6，9，4
> 
> **第一步:**分布均值 4 = 7
> **第二步:**求和(x–x .均值())**2 = 178
> **第三步:**求均值= 178 /20 = 8.9
> 这个结果就是**方差**。

> **参数:**
> **arr:**【array _ like】输入数组。
> **轴:**【int 或 int 的元组】轴，我们要沿着该轴计算方差。否则会认为`arr` 被展平(在所有轴上工作)。axis = 0 表示沿列的方差，axis = 1 表示沿行的方差。
> **out:**【n 数组，可选】我们要放置结果的不同数组。数组必须具有与预期输出相同的维度。
> **数据类型:**【数据类型，可选】计算方差时我们想要的类型。
> 
> **结果:**数组的方差(如果轴为无，则为标量值)或沿指定轴有方差值的数组；同时忽略 NaN 值。

**代码#1:**

```py
# Python Program illustrating 
# numpy.nanvar() method 
import numpy as np 

# 1D array 
arr = [20, 2, np.nan, 1, 34] 

print("arr : ", arr) 
print("\nnanvar of arr : ", np.nanvar(arr)) 

print("var of arr : ", np.var(arr)) 

print("\nnanvar of arr : ", np.nanvar(arr, dtype = np.float32)) 
print("var of arr : ", np.var(arr, dtype = np.float32)) 

```

**输出:**

```py
arr :  [20, 2, nan, 1, 34]

nanvar of arr :  187.1875
var of arr :  nan

nanvar of arr :  187.1875
var of arr :  nan
```

**代码#2:**

```py
# Python Program illustrating 
# numpy.nanvar() method 
import numpy as np 

# 2D array 
arr = [[2, 2, 2, 2, 2], 
    [15, 6, np.nan, 8, 2], 
    [23, 2, 54, 1, 2, ], 
    [np.nan, 44, 34, 7, 2]] 

# nanvar of the flattened array 
print("\nnanvar of arr, axis = None : ", np.nanvar(arr)) 

print("\nvar of arr, axis = None : ", np.var(arr)) 

# nanvar along the axis = 0 
print("\nnanvar of arr, axis = 0 : \n", np.nanvar(arr, axis = 0)) 

print("\nvar of arr, axis = 0 : ", np.var(arr, axis = 0)) 

# nanvar along the axis = 1 
print("\nnanvar of arr, axis = 1 : ", np.nanvar(arr, axis = 1)) 
```

**输出:**

```py
nanvar of arr, axis = None :  249.88888888888889

var of arr, axis = None :  nan

nanvar of arr, axis = 0 : 
 [ 74.88888889 312.75       458.66666667   9.25         0\.        ]

var of arr, axis = 0 :  [   nan 312.75    nan   9.25   0\.  ]

nanvar of arr, axis = 1 :  [  0\.      22.1875 421.84   313.1875]
```