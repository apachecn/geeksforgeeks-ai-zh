# Python | Numpy np.legadd()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-legad-method/](https://www.geeksforgeeks.org/python-numpy-np-legadd-method/)

`**np.legadd()**`法是将一个**勒让德系列**加到另一个上。它返回两个**勒让德级数** `c1 + c2.`的和

> **语法:** `np.legadd(c1, c2)`
> **参数:**
> **c1、C2:**【array _ like】勒让德级数系数的一维数组从低到高排序。
> 
> **返回:**【ndarray】表示它们之和的勒让德级数的数组。

**代码#1 :**

```py
# Python program explaining
# numpy.legadd() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Legendre series coefficients
s1 = (1, 3, 5) 
s2 = (2, 4, 6)    

# using np.legadd() method 
res = geek.legadd(s1, s2) 

# Resulting legendre series
print (res) 
```

**Output:**

```py
[  3\.   7\.  11.]

```

**代码#2 :**

```py
# Python program explaining
# numpy.legadd() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Legendre series coefficients
s1 = (10, 20, 30, 40, 50) 
s2 = (2, 4, 6, 8, 10)    

# using np.legadd() method 
res = geek.legadd(s1, s2) 

# Resulting legendre series
print (res) 
```

**Output:**

```py
[ 12\.  24\.  36\.  48\.  60.]

```