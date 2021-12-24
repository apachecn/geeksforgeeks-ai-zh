# numpy | Random _ integers()函数中的随机采样

> 原文:[https://www . geesforgeks . org/random-sampling-in-numpy-random _ integers-function/](https://www.geeksforgeeks.org/random-sampling-in-numpy-random_integers-function/)

**`numpy.random.random_integers()`** 是 numpy 中做随机抽样的功能之一。它返回一个指定形状的数组，并用从低(包括)到高(不包括)的随机整数填充，即在间隔`[low, high).`内

> **语法:**numpy . random . random _ 整数(低，高=无，大小=无)
> 
> **参数:**
> **低:**【int】从分布中抽取的最低(有符号)整数。但是，如果 high=None，它作为样本中的最高整数工作。
> **高:**【int，可选】从分布中抽取的最大(有符号)整数。
> **大小:**【int 或 int 元组，可选】输出形状。如果给定的形状是例如(m，n，k)，则绘制 m * n * k 个样本。默认值为无，在这种情况下，将返回一个值。
> 
> **返回:**区间内的随机整数数组`[low, high)`或单个这样的随机整数(如果未提供大小)。

**代码#1 :**

```
# Python program explaining
# numpy.random.random_integers() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.random_integers(low = 0, high = 5, size = 4)
print ("Output 1D Array filled with random integers : ", out_arr) 
```

**Output :**

```
Output 1D Array filled with random integers :  [1 1 4 1]

```

**代码#2 :**

```
# Python program explaining
# numpy.random.random_integers() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.random_integers(low = 3, size =(3, 3))
print ("Output 2D Array filled with random integers : ", out_arr) 
```

**Output :**

```
Output 2D Array filled with random integers :  [[2 3 1]
 [2 2 3]
 [3 3 3]]

```

**代码#3 :**

```
# Python program explaining
# numpy.random.random_integers() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.random_integers(1, 6, (2, 2, 3))
print ("Output 3D Array filled with random integers : ", out_arr) 
```

**Output :**

```
Output 3D Array filled with random integers :  [[[4 8 5 7]
Output 3D Array filled with random integers :  [[[5 1 5]
  [5 4 1]]

 [[3 6 4]
  [4 5 3]]]

```