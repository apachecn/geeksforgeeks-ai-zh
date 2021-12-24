# numpy | Random()函数中的随机采样

> 原文:[https://www . geesforgeks . org/random-sampling-in-numpy-random-function/](https://www.geeksforgeeks.org/random-sampling-in-numpy-random-function/)

**`numpy.random.random()`** 是 numpy 中做随机抽样的功能之一。它返回一个指定形状的数组，并在半开间隔`[0.0, 1.0).`内用随机浮动填充它

> **语法:** numpy.random.random(大小=无)
> 
> **参数:**
> **大小:**【int 或 int 元组，可选】输出形状。如果给定的形状是例如(m，n，k)，则绘制 m * n * k 个样本。默认值为无，在这种情况下，将返回一个值。
> 
> **返回:**间隔内的随机浮动数组`[0.0, 1.0).`或单个此类随机浮动(如果未提供大小)。

**代码#1 :**

```py
# Python program explaining
# numpy.random.random() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.random(size = 3)
print ("Output 1D Array filled with random floats : ", out_arr) 
```

**Output :**

```py
Output 1D Array filled with random floats :  [ 0.21698734  0.01617363  0.70382199]

```

**代码#2 :**

```py
# Python program explaining
# numpy.random.random() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.random(size =(2, 4))
print ("Output 2D Array filled with random floats : ", out_arr) 
```

**Output :**

```py
Output 2D Array filled with random floats :  [[ 0.95423066  0.35595927  0.76048569  0.90163066]
 [ 0.41903408  0.85596254  0.21666156  0.05734769]]

```

**代码#3 :**

```py
# Python program explaining
# numpy.random.random() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.random((2, 3, 2))
print ("Output 3D Array filled with random floats : ", out_arr) 
```

**Output :**

```py
Output 3D Array filled with random floats :  [[[ 0.07861816  0.79132387]
  [ 0.9112629   0.98162851]
  [ 0.0727613   0.03480279]]

 [[ 0.11267727  0.07631742]
  [ 0.47554553  0.83625053]
  [ 0.67781339  0.37856642]]]

```