# Python | Numpy NP . lag company()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag companion-method/](https://www.geeksforgeeks.org/python-numpy-np-lagcompanion-method/)

`**np.lagcompanion()**`方法用于返回**拉盖尔**系列的伴矩阵。

> **语法:** `np.lagcompanion(c)`
> **参数:**
> **c:**【array _ like】从低到高排序的拉盖尔级数系数一维数组。
> 
> **返回:**【n 数组】维度的伴随矩阵(度，度)。

**代码#1 :**

```py
# Python program explaining
# numpy.lagcompanion() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Input laguerre series coefficients

s = (2, 4, 8) 

# using np.lagcompanion() method 
res = geek.lagcompanion(s) 

# Resulting Companion matrix
print (res) 
```

**Output:**

```py
[[ 1\.  -0.5]
 [-1\.   4\. ]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.lagcompanion() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients
s = (1, 2, 3, 4, 5) 

# using np.lagcompanion() method 
res = geek.lagcompanion(s) 

# Resulting Companion matrix
print (res) 
```

**Output:**

```py
[[  1\.   -1\.    0\.    0.8]
 [ -1\.    3\.   -2\.    1.6]
 [  0\.   -2\.    5\.   -0.6]
 [  0\.    0\.   -3\.   10.2]]

```