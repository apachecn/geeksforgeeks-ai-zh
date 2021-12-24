# numpy 矩阵运算| repmat()函数

> 原文:[https://www . geesforgeks . org/numpy-matrix-operations-repmat-function/](https://www.geeksforgeeks.org/numpy-matrix-operations-repmat-function/)

**`numpy.matlib.repmat()`** 是 numpy 中做矩阵运算的另一个功能。它返回重复 0 维、1 维或 2 维数组或矩阵 M×N 次。

> **语法:**num py . MATLAB . rep mat(a、m、n)
> 
> **参数:**
> **a:**【array _ like】要重复的输入数组或矩阵。
> **m，n:**【int】a 沿第一轴和第二轴重复的次数。
> 
> **返回:**【n 数组】重复数组。

**代码#1 :**

```
# Python program explaining
# numpy.matlib.repmat() function

# importing numpy and matrix library
import numpy as geek
import numpy.matlib

# creating input array using  
# array function 
in_arr = geek.array([[1, 0, 2], [3, 4, 5]])
print("Input array", in_arr) 

# making a new array 
# using repmat() function 
out_mat = geek.matlib.repmat(in_arr, 2, 3) 
print ("Output repeated matrix : ", out_mat) 
```

**Output :**

```
Input array [[1 0 2]
 [3 4 5]]
Output repeated matrix :  [[1 0 2 1 0 2 1 0 2]
 [3 4 5 3 4 5 3 4 5]
 [1 0 2 1 0 2 1 0 2]
 [3 4 5 3 4 5 3 4 5]]

```

**代码#2 :**

```
# Python program explaining
# numpy.matlib.repmat() function

# importing numpy and matrix library
import numpy as geek
import numpy.matlib

# creating input array using  
# arange function 
in_arr = geek.arange(3)
print("Input array", in_arr) 

# making a new array 
# using repmat() function 
out_mat = geek.matlib.repmat(in_arr, 2, 2) 
print ("Output repeated matrix : ", out_mat) 
```

**Output :**

```
Input array [0 1 2]
Output repeated matrix :  [[0 1 2 0 1 2]
 [0 1 2 0 1 2]]

```