# Python | Numpy np.legroots()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-leg root-method/](https://www.geeksforgeeks.org/python-numpy-np-legroots-method/)

`**np.legroots()**`方法用于计算**勒让德级数**的根。返回多项式的根。

> **语法:** `np.legroots(c)`
> **参数:**
> **c:**【array _ like】勒让德级数系数的一维数组。
> 
> **返回:**【ndarray】系列根的数组。如果所有的根都是真实的，那么出来也是真实的，否则就是复杂的。

**代码#1 :**

```py
# Python program explaining
# numpy.legroots() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Input legendre series coefficients

s = (2, 4, 8) 

# using np.legroots() method 
res = geek.legroots(s) 

# Resulting legendre series coefficient
print (res) 
```

**Output:**

```py
[-0.60762522  0.27429189]

```

**代码#2 :**

```py
# Python program explaining
# numpy.legroot() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# legendre series coefficients
s = (1, 2, 3, 4, 5) 

# using np.legroots() method 
res = geek.legroots(s) 

# Resulting legendre series
print (res) 
```

**Output:**

```py
[-0.86884116 -0.48972874  0.21530729  0.68611975]

```