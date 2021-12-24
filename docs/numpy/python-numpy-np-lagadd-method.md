# Python | Numpy np.lagadd()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag add-method/](https://www.geeksforgeeks.org/python-numpy-np-lagadd-method/)

`**np.lagadd()**`法是将一个**拉盖尔系列**加到另一个上。它返回两个**拉盖尔级数**和`c1 + c2.`的和

> **语法:** `np.lagadd(c1, c2)`
> **参数:**
> **c1、C2:**【array _ like】从低到高排序的拉盖尔级数系数一维数组。
> 
> **返回:**【ndarray】表示它们之和的拉盖尔级数的数组。

**代码#1 :**

```
# Python program explaining
# numpy.lagadd() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients
s1 = (1, 3, 5) 
s2 = (2, 4, 6)    

# using np.lagadd() method 
res = geek.lagadd(s1, s2) 

# Resulting laguerre series
print (res) 
```

**Output:**

```
[  3\.   7\.  11.]

```

**代码#2 :**

```
# Python program explaining
# numpy.lagadd() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Laguerre series coefficients
s1 = (10, 20, 30, 40, 50) 
s2 = (2, 4, 6, 8, 10)    

# using np.lagadd() method 
res = geek.lagadd(s1, s2) 

# Resulting laguerre series
print (res) 
```

**Output:**

```
[ 12\.  24\.  36\.  48\.  60.]

```