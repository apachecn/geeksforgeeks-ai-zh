# Python | Numpy np.lagder()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag der-method/](https://www.geeksforgeeks.org/python-numpy-np-lagder-method/)

`**np.lagroots()**`方法用于区分一个**拉盖尔**系列。

> **语法:** `np.lagder(c, m=1, scl=1, axis=0)`
> **参数:**
> **c:**【array _ like】从低到高排序的拉盖尔级数系数一维数组。
> **m:**【int，可选】取的导数个数，必须非负。默认值为 1。
> **scl :** 【标量，可选】每次微分都乘以 scl。默认值为 1。
> **轴:**【int，可选】取导数的轴。默认值为 0。
> 
> **返回:**【ndarray】导数的拉盖尔级数。

**代码#1 :**

```py
# Python program explaining
# numpy.lagder() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Input laguerre series coefficients

s = (2, 4, 8) 

# using np.lagder() method 
res = geek.lagder(s) 

# Resulting laguerre series coefficient
print (res) 
```

**Output:**

```py
[-12\.  -8.]

```

**代码#2 :**

```py
# Python program explaining
# numpy.lagder() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients
s = (1, 2, 3, 4, 5) 

# using np.lagder() method 
res = geek.lagder(s, m = 2, scl = 0.5) 

# Resulting laguerre series
print (res) 
```

**Output:**

```py
[ 6.5   3.5   1.25]

```