# Python | Numpy 多项式 lagline()方法

> 原文:[https://www . geesforgeks . org/python-numpy-多项式-lagline-method/](https://www.geeksforgeeks.org/python-numpy-polynomial-lagline-method/)

`**np.lagline()**`方法用来寻找一个**拉盖尔级数**，其图形是一条直线。

> **语法:** `np.lagline(off, scl)`
> **参数:**
> **off，scl :** 【标量】指定行由 off + scl*x 给出。
> 
> **返回:**【ndarray】结果行的拉盖尔级数系数数组。

**代码#1 :**

```py
# Python program explaining 
# numpy.lagline() method  

# importing numpy as np   
# and numpy.polynomial.laguerre module as geek  
import numpy as np  
import numpy.polynomial.laguerre as geek 

# using np.lagline() method  
res = geek.lagline(2, 3)  

# Resulting Laguerre series 
print (res)  
```

**Output:**

```py
[ 5 -3]

```

**代码#2 :**

```py
# Python program explaining 
# numpy.lagline() method  

# importing numpy as np   
# and numpy.polynomial.laguerre module as geek  
import numpy as np  
import numpy.polynomial.laguerre as geek 

# using np.lagline() method  
res = geek.lagline(1, 4)  

# Resulting laguerre series 
print (res)
```

**Output:**

```py
[ 5 -4]

```