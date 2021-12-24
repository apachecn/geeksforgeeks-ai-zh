# Python | Numpy np.legmul()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-legmul-method/](https://www.geeksforgeeks.org/python-numpy-np-legmul-method/)

`**np.legmul()**`法是将一个**勒让德级数**相乘得到另一个。它返回两个**勒让德系列** `c1 * c2.`的乘积

> **语法:** `np.legmul(c1, c2)`
> **参数:**
> **c1、C2:**【array _ like】勒让德级数系数的一维数组从低到高排序。
> 
> **返回:**【ndarray】表示它们乘积的勒让德级数系数。

**代码#1 :**

```py
# Python program explaining
# numpy.legmul() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Legendre series coefficients

s1 = (2, 4, 8) 
s2 = (1, 3, 5)   

# using np.legmul() method 
res = geek.legmul(s1, s2) 

# Resulting Legendre series
print (res) 
```

**Output:**

```py
[ 14\.          27.6         37.42857143  26.4         20.57142857]

```

**代码#2 :**

```py
# Python program explaining
# numpy.legmul() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Legendre series coefficients
s1 = (10, 20, 30, 40, 50) 
s2 = (2, 4, 6, 8, 10)    

# using np.legmul() method 
res = geek.legmul(s1, s2) 

# Resulting Legendre series
print (res) 
```

**Output:**

```py
[ 183.93650794  451.80952381  666.43578644  755.23232323  786.997003
  626.61782662  512.26551227  326.34032634  190.36519037]

```