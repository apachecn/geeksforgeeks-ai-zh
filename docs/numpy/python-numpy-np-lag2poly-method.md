# Python | Numpy np.lag2poly()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag 2 poly-method/](https://www.geeksforgeeks.org/python-numpy-np-lag2poly-method/)

`**np.lag2poly()**`方法用于将拉盖尔级数转化为多项式。

> **语法:** `np.lag2poly(c)`
> **参数:**
> **c:**【array _ like】从低到高排序的拉盖尔级数系数一维数组。
> 
> **返回:**【n 数组】包含等价多项式系数的一维数组。

**代码#1 :**

```py
# Python program explaining
# numpy.lag2poly() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Input laguerre series coefficients

c = np.array([0.1, 0.2, 0.3, 0.4, 0.5]) 

# using np.lag2poly() method 
res = geek.lag2poly(c) 

# Resulting equivalent polynomial series coefficient
print (res) 
```

**Output:**

```py
[ 1.5        -4\.          2.25       -0.4         0.02083333]

```

**代码#2 :**

```py
# Python program explaining
# numpy.lag2poly() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Input laguerre series coefficients

c = ( 1, 2, 3, 4, 5)

# using np.lag2poly() method 
res = geek.lag2poly(c) 

# Resulting equivalent polynomial series coefficient
print (res) 
```

**Output:**

```py
[ 15\.         -40\.          22.5         -4\.           0.20833333]

```