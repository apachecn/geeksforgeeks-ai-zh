# Python | Numpy NP . lag root()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag root-method/](https://www.geeksforgeeks.org/python-numpy-np-lagroots-method/)

`**np.lagroots()**`方法用于计算一个**拉盖尔级数**的根。返回多项式的根。

> **语法:** `np.lagroots(c)`
> **参数:**
> **c:**【array _ like】从低到高排序的拉盖尔级数系数一维数组。
> 
> **返回:**【ndarray】系列根的数组。如果所有的根都是真实的，那么出来也是真实的，否则就是复杂的。

**代码#1 :**

```
# Python program explaining
# numpy.lagroots() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Input laguerre series coefficients

s = (2, 4, 8) 

# using np.lagroots() method 
res = geek.lagroots(s) 

# Resulting laguerre series coefficient
print (res) 
```

**Output:**

```
[ 0.8416876  4.1583124]

```

**代码#2 :**

```
# Python program explaining
# numpy.lagroot() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients
s = (1, 2, 3, 4, 5) 

# using np.lagroots() method 
res = geek.lagroots(s) 

# Resulting laguerre series
print (res) 
```

**Output:**

```
[  0.50680523   2.37919156   5.5446037   10.76939951]

```