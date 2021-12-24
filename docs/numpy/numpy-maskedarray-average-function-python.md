# Numpy maskearray . average()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-average-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-average-function-python/)

**`numpy.MaskedArray.average()`** 函数用于返回给定轴上数组的加权平均值。

> **语法:** `numpy.ma.average(arr, axis=None, weights=None, returned=False)`
> 
> **参数:**
> 
> **arr:**【array _ like】输入要平均其数据的屏蔽数组。计算中不考虑屏蔽条目。
> **轴:**【整数，可选】平均 arr 所沿的轴。如果“无”，则对展平的数组进行平均。
> **权重:**【array _ like，可选】每个元素在平均值计算中的重要性。如果权重=无，则假定 arr 中的所有数据的权重都等于 1。如果权重很复杂，虚部将被忽略。
> **返回:**【bool，可选】表示元组(结果，权重之和)是作为输出返回(True)，还是只返回结果(False)。默认值为假。
> 
> **返回:**【标量或掩码数组】沿指定轴的平均值。当返回为真时，返回一个元组，平均值作为第一个元素，权重之和作为第二个元素。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.average() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array  
in_arr = geek.array([[1, 2], [ 3, -1], [ 5, -3]])
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making  entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[1, 0], [ 1, 0], [ 0, 0]]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.average    
# methods to masked array
out_arr = ma.average(mask_arr) 
print ("normal average of masked array : ", out_arr) 
```

**Output:**

```
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
normal average of masked array :  0.75

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.average() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array  
in_arr = geek.array([[1, 2], [ 3, -1], [ 5, -3]])
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making  entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[1, 0], [ 1, 0], [ 0, 0]]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.average    
# methods to masked array
out_arr = ma.average(mask_arr, weights =[[0, 1], [ 0, 2], [ 3, 1]]) 
print ("weighted average of masked array : ", out_arr) 
```

**Output:**

```
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
weighted average of masked array :  1.7142857142857142

```