# Python | Numpy np.lagdiv()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag div-method/](https://www.geeksforgeeks.org/python-numpy-np-lagdiv-method/)

`**np.lagdiv()**`法是将一个**拉盖尔级数**划分为另一个。它返回两个**拉盖尔级数** `c1 / c2.`的余数商

> **语法:** `np.lagdiv(c1, c2)`
> **参数:**
> **c1、C2:**【array _ like】从低到高排序的拉盖尔级数系数一维数组。
> 
> **返回:**【ndarray】代表商和余数的拉盖尔级数系数。

**代码#1 :**

```
# Python program explaining
# numpy.lagdiv() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients

s1 = (2, 4, 8) 
s2 = (1, 3, 5)   

# using np.lagdiv() method 
res = geek.lagdiv(s1, s2) 

# Resulting laguerre series
print (res) 
```

**Output:**

```
(array([ 1.6]), array([ 0.4, -0.8]))

```

**代码#2 :**

```
# Python program explaining
# numpy.lagdiv() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients
s1 = (10, 20, 30, 40, 50) 
s2 = (2, 4, 6, 8, 10)    

# using np.lagdiv() method 
res = geek.lagdiv(s1, s2) 

# Resulting laguerre series
print (res) 
```

**Output:**

```
(array([ 5.]), array([ 0.]))

```