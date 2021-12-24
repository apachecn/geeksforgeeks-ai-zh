# Python | Numpy np.lagfromroots()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-NP-lagforroots-method/](https://www.geeksforgeeks.org/python-numpy-np-lagfromroots-method/)

`**np.lagfromroots()**`方法用于生成具有给定根的**拉盖尔**序列。

> **语法:** `np.lagfromroots(roots)`
> **参数:**
> **根:**【array _ like】输入包含根的序列。
> 
> **返回:**【n 数组】拉盖尔级数的一维系数数组。

**代码#1 :**

```
# Python program explaining
# numpy.lagfromroots() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Input roots

roots = (2, 4, 8) 

# using np.lagfromroots() method 
res = geek.lagfromroots(roots) 

# Resulting laguerre series coefficient
print (res) 
```

**Output:**

```
[-30\. -18\. -10\.  -6.]

```

**代码#2 :**

```
# Python program explaining
# numpy.lagfromroots() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Input roots
s = (1, 2, 3, 4, 5) 

# using np.lagfromroots() method 
res = geek.lagfromroots(s) 

# Resulting laguerre series coefficient
print (res) 
```

**Output:**

```
[ -26\.  -64\.  120\. -270\.  240\. -120.]

```