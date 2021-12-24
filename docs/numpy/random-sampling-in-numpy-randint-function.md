# numpy | randint()函数中的随机采样

> 原文:[https://www . geesforgeks . org/random-sampling-in-numpy-randint-function/](https://www.geeksforgeeks.org/random-sampling-in-numpy-randint-function/)

**`numpy.random.randint()`** 是 numpy 中做随机抽样的功能之一。它返回一个指定形状的数组，并用从低(包括)到高(不包括)的随机整数填充，即在间隔`[low, high).`内

> **语法:** numpy.random.randint(低，高=无，大小=无，数据类型='l ')
> 
> **参数:**
> **低:**【int】从分布中抽取的最低(有符号)整数。但是，如果 high=None，它作为样本中的最高整数工作。
> **高:**【int，可选】从分布中抽取的最大(有符号)整数。
> **大小:**【int 或 int 元组，可选】输出形状。如果给定的形状是例如(m，n，k)，则绘制 m * n * k 个样本。默认值为无，在这种情况下，将返回一个值。
> **数据类型:**【可选】所需的输出数据类型。
> 
> **返回:**区间内的随机整数数组`[low, high)`或单个这样的随机整数(如果未提供大小)。

**代码#1 :**

```
# Python program explaining
# numpy.random.randint() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.randint(low = 0, high = 3, size = 5)
print ("Output 1D Array filled with random integers : ", out_arr) 
```

**Output :**

```
Output 1D Array filled with random integers :  [1 1 0 1 1]

```

**代码#2 :**

```
# Python program explaining
# numpy.random.randint() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.randint(low = 4, size =(2, 3))
print ("Output 2D Array filled with random integers : ", out_arr) 
```

**Output :**

```
Output 2D Array filled with random integers :  [[1 1 0]
 [1 0 3]]

```

**代码#3 :**

```
# Python program explaining
# numpy.random.randint() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.randint(2, 10, (2, 3, 4))
print ("Output 3D Array filled with random integers : ", out_arr) 
```

**Output :**

```
Output 3D Array filled with random integers :  [[[4 8 5 7]
  [6 5 6 7]
  [4 3 4 3]]

 [[2 9 2 2]
  [3 2 2 3]
  [6 8 3 2]]]

```