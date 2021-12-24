# Python | Numpy np.legsub()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-legsub-method/](https://www.geeksforgeeks.org/python-numpy-np-legsub-method/)

`**np.legub()**`法是将一个**勒让德级数**减去另一个。它返回两个**勒让德系列** `c1 - c2.`的差值

> **语法:** `np.legub(c1, c2)`
> **参数:**
> **c1、C2:**【array _ like】勒让德级数系数的一维数组从低到高排序。
> 
> **返回:**【ndarray】表示它们之差的勒让德级数系数。

**代码#1 :**

```py
# Python program explaining
# numpy.legsub() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Legendre series coefficients

s1 = (2, 4, 8) 
s2 = (1, 3, 5)   

# using np.legsub() method 
res = geek.legsub(s1, s2) 

# Resulting Legendre series
print (res) 
```

**Output:**

```py
[ 1\.  1\.  3.]

```

**代码#2 :**

```py
# Python program explaining
# numpy.legub() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Legendre series coefficients
s1 = (10, 20, 30, 40, 50) 
s2 = (2, 4, 6, 8, 10)    

# using np.legsub() method 
res = geek.legsub(s1, s2) 

# Resulting Legendre series
print (res) 
```

**Output:**

```py
[  8\.  16\.  24\.  32\.  40.]

```