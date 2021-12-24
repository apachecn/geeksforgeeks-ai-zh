# numpy | ranf()函数中的随机采样

> 原文:[https://www . geesforgeks . org/random-sampling-in-numpy-ranf-function/](https://www.geeksforgeeks.org/random-sampling-in-numpy-ranf-function/)

**`numpy.random.ranf()`** 是 numpy 中做随机抽样的功能之一。它返回一个指定形状的数组，并在半开间隔`[0.0, 1.0).`内用随机浮动填充它

> **语法:** numpy.random.ranf(大小=无)
> 
> **参数:**
> **大小:**【int 或 int 元组，可选】输出形状。如果给定的形状是例如(m，n，k)，则绘制 m * n * k 个样本。默认值为无，在这种情况下，将返回一个值。
> 
> **返回:**间隔内的随机浮动数组`[0.0, 1.0).`或单个此类随机浮动(如果未提供大小)。

**代码#1 :**

```py
# Python program explaining
# numpy.random.ranf() function

# importing numpy
import numpy as geek

# output random float value
out_val = geek.random.ranf()
print ("Output random float value : ", out_val) 
```

**Output :**

```py
Output random float value :  0.0877051588430926

```

**代码#2 :**

```py
# Python program explaining
# numpy.random.ranf() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.ranf(size =(2, 1))
print ("Output 2D Array filled with random floats : ", out_arr) 
```

**Output :**

```py
Output 2D Array filled with random floats :  [[ 0.14186407]
 [ 0.58068259]]

```

**代码#3 :**

```py
# Python program explaining
# numpy.random.ranf() function

# importing numpy
import numpy as geek

# output array
out_arr = geek.random.ranf((3, 3, 2))
print ("Output 3D Array filled with random floats : ", out_arr) 
```

**Output :**

```py
Output 3D Array filled with random floats :  [[[ 0.11013584  0.67844746]
  [ 0.84691569  0.09467084]
  [ 0.69918864  0.12137178]]

 [[ 0.30629051  0.28301093]
  [ 0.1302665   0.2196221 ]
  [ 0.51555358  0.73191852]]

 [[ 0.72806359  0.66485275]
  [ 0.80654791  0.04947181]
  [ 0.06380535  0.99306064]]]

```