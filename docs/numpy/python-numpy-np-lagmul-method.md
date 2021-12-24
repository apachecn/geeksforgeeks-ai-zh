# Python | Numpy np.lagmul()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag mul-method/](https://www.geeksforgeeks.org/python-numpy-np-lagmul-method/)

`**np.lagmul()**`法是将一个**拉盖尔级数**相乘得到另一个。它返回两个**拉盖尔系列**和`c1 * c2.`的乘积

> **语法:** `np.lagmul(c1, c2)`
> **参数:**
> **c1、C2:**【array _ like】从低到高排序的拉盖尔级数系数一维数组。
> 
> **返回:**【ndarray】代表它们乘积的拉盖尔级数系数。

**代码#1 :**

```
# Python program explaining
# numpy.lagmul() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients

s1 = (2, 4, 8) 
s2 = (1, 3, 5)   

# using np.lagmul() method 
res = geek.lagmul(s1, s2) 

# Resulting laguerre series
print (res) 
```

**Output:**

```
[  54\.  -86\.  266\. -348\.  240.]

```

**代码#2 :**

```
# Python program explaining
# numpy.lagmul() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients
s1 = (10, 20, 30, 40, 50) 
s2 = (2, 4, 6, 8, 10)    

# using np.lagmul() method 
res = geek.lagmul(s1, s2) 

# Resulting laguerre series
print (res) 
```

**Output:**

```
[   1100\.   -1600\.   10400\.  -36000\.   90600\. -152400\.  169400\. -112000.
   35000.]

```