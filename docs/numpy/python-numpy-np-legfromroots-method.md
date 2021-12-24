# Python | Numpy NP . legfroroots()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-legfrom root-method/](https://www.geeksforgeeks.org/python-numpy-np-legfromroots-method/)

`**np.legfromroots()**`方法用于生成给定根的**勒让德**级数。

> **语法:** `np.legfromroots(roots)`
> **参数:**
> **根:**【array _ like】输入包含根的序列。
> 
> **返回:**【n 数组】勒让德级数的一维系数数组。

**代码#1 :**

```py
# Python program explaining
# numpy.legfromroots() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Input roots

roots = (2, 4, 8) 

# using np.legfromroots() method 
res = geek.legfromroots(roots) 

# Resulting legendre series coefficient
print (res) 
```

**Output:**

```py
[-68.66666667  56.6         -9.33333333   0.4       ]

```

**代码#2 :**

```py
# Python program explaining
# numpy.legfromroots() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Input roots
s = (1, 2, 3, 4, 5) 

# using np.legfromroots() method 
res = geek.legfromroots(s) 

# Resulting legendre series coefficient
print (res) 
```

**Output:**

```py
[ -1.98000000e+02   3.25428571e+02  -1.58571429e+02   3.44444444e+01
  -3.42857143e+00   1.26984127e-01]

```