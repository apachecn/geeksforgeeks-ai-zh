# Python | Numpy np.lagsub()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag sub method/](https://www.geeksforgeeks.org/python-numpy-np-lagsub-method/)

`**np.lagub()**`法是将一个**拉盖尔级数**减去另一个。它返回两个**拉盖尔系列**T1】的差值

> **语法:** `np.lagub(c1, c2)`
> **参数:**
> **c1、C2:**【array _ like】从低到高排序的拉盖尔级数系数一维数组。
> 
> **返回:**【ndarray】代表其差值的拉盖尔级数系数。

**代码#1 :**

```py
# Python program explaining
# numpy.lagsub() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients

s1 = (2, 4, 8) 
s2 = (1, 3, 5)   

# using np.lagsub() method 
res = geek.lagsub(s1, s2) 

# Resulting laguerre series
print (res) 
```

**Output:**

```py
[ 1\.  1\.  3.]

```

**代码#2 :**

```py
# Python program explaining
# numpy.lagub() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients
s1 = (10, 20, 30, 40, 50) 
s2 = (2, 4, 6, 8, 10)    

# using np.lagsub() method 
res = geek.lagsub(s1, s2) 

# Resulting laguerre series
print (res) 
```

**Output:**

```py
[  8\.  16\.  24\.  32\.  40.]

```