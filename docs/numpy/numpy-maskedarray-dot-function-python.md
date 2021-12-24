# Numpy maskearray . dot()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-dot-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-dot-function-python/)

**`numpy.MaskedArray.dot()`** 函数用于计算两个掩膜阵列的点积。

> **语法:** `numpy.ma.dot(arr1, arr2, strict=False)`
> 
> **参数:**
> **arr1、arr 2:**【ndarray】输入数组。
> **严格:**【bool，可选】屏蔽数据是传播(True)还是设置为 0 (False)进行计算。默认值为假。
> 
> **返回:**【ndarray】arr 1 和 arr2 的点积。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.dot() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input arrays   
in_arr1 = geek.array([[1, 2], [ 3, 4]])
print ("1st Input array : ", in_arr1) 

in_arr2 = geek.array([[-1, -2], [ -3, -4]]) 
print ("2nd Input array : ", in_arr2) 

# Now we are creating  masked array.  
# by making  entry as invalid   
mask_arr1 = ma.masked_array(in_arr1, mask = [[ 1, 0], [ 0, 1]])  
print ("1st Masked array : ", mask_arr1) 

mask_arr2 = ma.masked_array(in_arr2, mask =[[ 0, 1], [ 0, 0]])  
print ("2nd Masked array : ", mask_arr2) 

# applying MaskedArray.dot methods  
# to masked array  
out_arr = ma.dot(mask_arr1, mask_arr2)  
print ("Dot product of two arrays : ", out_arr)      
```

**Output:**

```
1st Input array :  [[1 2]
 [3 4]]
2nd Input array :  [[-1 -2]
 [-3 -4]]
1st Masked array :  [[-- 2]
 [3 --]]
2nd Masked array :  [[-1 --]
 [-3 -4]]
Dot product of two arrays :  [[-6 -8]
 [-3 --]]

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.dot() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input arrays   
in_arr1 = geek.array([[1, 2], [ 3, -1], [ 5, -3]])
print ("1st Input array : ", in_arr1) 

in_arr2 = geek.array([[1, 0, 3], [ 4, 1, 6]]) 
print ("2nd Input array : ", in_arr2) 

# Now we are creating  masked array.  
# by making  entry as invalid   
mask_arr1 = ma.masked_array(in_arr1, mask = [[ 1, 0], [ 0, 1], [ 0, 0]])  
print ("1st Masked array : ", mask_arr1) 

mask_arr2 = ma.masked_array(in_arr2, mask =[[ 0, 0, 0], [ 0, 0, 1]])  
print ("2nd Masked array : ", mask_arr2) 

# applying MaskedArray.dot methods  
# to masked array  
out_arr = ma.dot(mask_arr1, mask_arr2)  
print ("Dot product of two arrays : ", out_arr)      
```

**Output:**

```
1st Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
2nd Input array :  [[1 0 3]
 [4 1 6]]
1st Masked array :  [[-- 2]
 [3 --]
 [5 -3]]
2nd Masked array :  [[1 0 3]
 [4 1 --]]
Dot product of two arrays :  [[8 2 --]
 [3 0 9]
 [-7 -3 15]]

```