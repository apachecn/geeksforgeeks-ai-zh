# Python | Numpy np.lagpow()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag pow-method/](https://www.geeksforgeeks.org/python-numpy-np-lagpow-method/)

`**np.lagpow()**`方法用于将**拉盖尔级数**提升到给定的幂。它将**拉盖尔系列** `c`提升为**功率。**

> **语法:** `np.lagpow(c, pow, maxpower=16)`
> **参数:**
> **c:**【array _ like】从低到高排序的拉盖尔级数系数一维数组。
> **功率:**【整数】该系列将要提升到的功率。
> **最大功率:**【整数，可选】最大允许功率。默认值为 16。
> 
> **回归:**【ndarray】拉盖尔系异能。

**代码#1 :**

```
# Python program explaining
# numpy.lagpow() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Input laguerre series coefficients

s = (2, 4, 8) 

# using np.lagpow() method 
res = geek.lagpow(s, pow = 3) 

# Resulting laguerre series coefficient
print (res) 
```

**Output:**

```
[   3176\.  -25680\.  100512\. -206592\.  246528\. -161280\.   46080.]

```

**代码#2 :**

```
# Python program explaining
# numpy.lagpow() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients
s = (1, 2, 3, 4, 5) 

# using np.lagpow() method 
res = geek.lagpow(s, pow = 4) 

# Resulting laguerre series
print (res) 
```

**Output:**

```
[  1.88268525e+08  -4.12583040e+09   4.24806624e+10  -2.72789533e+11
   1.22285197e+12  -4.05794076e+12   1.03122236e+13  -2.04726003e+13
   3.20914270e+13  -3.98546302e+13   3.90872742e+13  -2.99578594e+13
   1.75922875e+13  -7.65283919e+12   2.32607876e+12  -4.41441000e+11
   3.94143750e+10]

```