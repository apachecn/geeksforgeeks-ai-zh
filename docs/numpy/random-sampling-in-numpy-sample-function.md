# numpy | sample()函数中的随机采样

> 原文:[https://www . geesforgeks . org/random-sample-in-numpy-sample-function/](https://www.geeksforgeeks.org/random-sampling-in-numpy-sample-function/)

**`numpy.random.sample()`** 是 numpy 中做随机抽样的功能之一。它返回一个指定形状的数组，并在半开间隔`[0.0, 1.0).`内用随机浮动填充它

> **语法:** numpy.random.sample(大小=无)
> 
> **参数:**
> **大小:**【int 或 int 元组，可选】输出形状。如果给定的形状是例如(m，n，k)，则绘制 m * n * k 个样本。默认值为无，在这种情况下，将返回一个值。
> 
> **返回:**间隔内的随机浮动数组`[0.0, 1.0).`或单个此类随机浮动(如果未提供大小)。

**代码#1 :**

```
# Python program explaining
# numpy.random.sample() function

# importing numpy
import numpy as geek

# output random value
out_val = geek.random.sample()
print ("Output random value : ", out_val) 
```

**Output :**

```
Output random value :  0.9261509680895836

```

**代码#2 :**

```
# Python program explaining
# numpy.random.sample() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.sample(size =(3, 3))
print ("Output 2D Array filled with random floats : ", out_arr) 
```

**Output :**

```
Output 2D Array filled with random floats :  [[ 0.75908777  0.88295677  0.60979136]
 [ 0.68157065  0.75100312  0.08321613]
 [ 0.8360331   0.64808891  0.14731635]]

```

**代码#3 :**

```
# Python program explaining
# numpy.random.sample() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.sample((2, 2, 3))
print ("Output 3D Array filled with random floats : ", out_arr) 
```

**Output :**

```
Output 3D Array filled with random floats :  [[[ 0.3073475   0.75709465  0.86934712]
  [ 0.21953745  0.48138292  0.30686482]]

 [[ 0.48925625  0.60222083  0.14403257]
  [ 0.87030919  0.87298872  0.2222136 ]]]

```