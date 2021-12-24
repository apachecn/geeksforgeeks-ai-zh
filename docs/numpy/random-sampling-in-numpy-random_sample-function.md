# numpy | Random _ sample()函数中的随机采样

> 原文:[https://www . geesforgeks . org/random-sampling-in-numpy-random _ sample-function/](https://www.geeksforgeeks.org/random-sampling-in-numpy-random_sample-function/)

**`numpy.random.random_sample()`** 是 numpy 中做随机抽样的功能之一。它返回一个指定形状的数组，并在半开间隔`[0.0, 1.0).`内用随机浮动填充它

> **语法:** numpy.random.random_sample(大小=无)
> 
> **参数:**
> **大小:**【int 或 int 元组，可选】输出形状。如果给定的形状是例如(m，n，k)，则绘制 m * n * k 个样本。默认值为无，在这种情况下，将返回一个值。
> 
> **返回:**间隔内的随机浮动数组`[0.0, 1.0).`或单个此类随机浮动(如果未提供大小)。

**代码#1 :**

```py
# Python program explaining
# numpy.random.sample() function

# importing numpy
import numpy as geek

# output random value
out_val = geek.random.random_sample()
print ("Output random float value : ", out_val) 
```

**Output :**

```py
Output random float value :  0.9211987310893188

```

**代码#2 :**

```py
# Python program explaining
# numpy.random.random_sample() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.random_sample(size =(1, 3))
print ("Output 2D Array filled with random floats : ", out_arr) 
```

**Output :**

```py
Output 2D Array filled with random floats :  [[ 0.64325146  0.4699456   0.89895437]]

```

**代码#3 :**

```py
# Python program explaining
# numpy.random.random_sample() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.random_sample((3, 2, 1))
print ("Output 3D Array filled with random floats : ", out_arr) 
```

**Output :**

```py
Output 3D Array filled with random floats :  [[[ 0.78245025]
  [ 0.77736746]]

 [[ 0.54389267]
  [ 0.18491758]]

 [[ 0.97428409]
  [ 0.73729256]]]

```