# Python | Numpy np.leg2poly()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-leg 2 poly-method/](https://www.geeksforgeeks.org/python-numpy-np-leg2poly-method/)

`**np.leg2poly()**`方法用于将勒让德级数转化为多项式。

> **语法:** `np.leg2poly(c)`
> **参数:**
> **c:**【array _ like】勒让德级数系数的一维数组从低到高排序。
> 
> **返回:**【n 数组】包含等价多项式系数的一维数组。

**代码#1 :**

```
# Python program explaining
# numpy.leg2poly() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Input legendre series coefficients

c = np.array([0.1, 0.2, 0.3, 0.4, 0.5]) 

# using np.leg2poly() method 
res = geek.leg2poly(c) 

# Resulting equivalent polynomial series coefficient
print (res) 
```

**Output:**

```
[ 0.1375 -0.4    -1.425   1\.      2.1875]

```

**代码#2 :**

```
# Python program explaining
# numpy.leg2poly() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Input legendre series coefficients

c = ( 1, 2, 3, 4, 5)

# using np.leg2poly() method 
res = geek.leg2poly(c) 

# Resulting equivalent polynomial series coefficient
print (res) 
```

**Output:**

```
[  1.375  -4\.    -14.25   10\.     21.875]

```