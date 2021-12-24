# Python | Numpy NP . polyFromroots()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-NP-polyromroots-method/](https://www.geeksforgeeks.org/python-numpy-np-polyfromroots-method/)

`**np.polyfromroots()**`方法用于生成给定根的**多项式**级数。

> **语法:** `np.polyfromroots(roots)`
> **参数:**
> **根:**【array _ like】输入包含根的序列。
> 
> **返回:**【n 数组】多项式级数系数的一维数组。

**代码#1 :**

```py
# Python program explaining
# numpy.polyfromroots() method 

# importing numpy as np  
# and numpy.polynomial.polynomial module as geek 
import numpy as np 
import numpy.polynomial.polynomial as geek

# Input roots

roots = (2, 4, 8) 

# using np.polyfromroots() method 
res = geek.polyfromroots(roots) 

# Resulting polynomial series coefficient
print (res) 
```

**Output:**

```py
[-64\.  56\. -14\.   1.]

```

**代码#2 :**

```py
# Python program explaining
# numpy.polyfromroots() method 

# importing numpy as np  
# and numpy.polynomial.polynomial module as geek 
import numpy as np 
import numpy.polynomial.polynomial as geek

# Input roots
s = (1, 2, 3, 4, 5) 

# using np.polyfromroots() method 
res = geek.polyfromroots(s) 

# Resulting polynomial series coefficient
print (res) 
```

**Output:**

```py
[-120\.  274\. -225\.   85\.  -15\.    1.]

```