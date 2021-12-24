# Python | Numpy NP . legcompany()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-leg companion-method/](https://www.geeksforgeeks.org/python-numpy-np-legcompanion-method/)

`**np.legcompanion()**`方法用于返回**勒让德**系列的伴随矩阵。

> **语法:** `np.legcompanion(c)`
> **参数:**
> **c:**【array _ like】勒让德级数系数的一维数组从低到高排序。
> 
> **返回:**【n 数组】维度的伴随矩阵(度，度)。

**代码#1 :**

```py
# Python program explaining
# numpy.legcompanion() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Input legendre series coefficients

s = (2, 4, 8) 

# using np.legcompanion() method 
res = geek.legcompanion(s) 

# Resulting Companion matrix
print (res) 
```

**Output:**

```py
[[ 0\.          0.28867513]
 [ 0.57735027 -0.33333333]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.legcompanion() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# legendre series coefficients
s = (1, 2, 3, 4, 5) 

# using np.legcompanion() method 
res = geek.legcompanion(s) 

# Resulting Companion matrix
print (res) 
```

**Output:**

```py
[[ 0\.          0.57735027  0\.         -0.30237158]
 [ 0.57735027  0\.          0.51639778 -0.34914862]
 [ 0\.          0.51639778  0\.          0.10141851]
 [ 0\.          0\.          0.50709255 -0.45714286]]

```