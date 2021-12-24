# Python | Numpy 多项式 legline()方法

> 原文:[https://www . geesforgeks . org/python-numpy-多项式-legline-method/](https://www.geeksforgeeks.org/python-numpy-polynomial-legline-method/)

`**np.legline()**`法求一个**勒让德级数**其图形为直线。

> **语法:** `np.legline(off, scl)`
> **参数:**
> **off，scl :** 【标量】指定行由 off + scl*x 给出。
> 
> **返回:**【ndarray】结果行的勒让德级数系数数组。

**代码#1 :**

```
# Python program explaining 
# numpy.legline() method  

# importing numpy as np   
# and numpy.polynomial.legendre module as geek  
import numpy as np  
import numpy.polynomial.legendre as geek 

# using np.legline() method  
res = geek.legline(2, 3)  

# Resulting legendre series 
print (res)  
```

**Output:**

```
[2 3]

```

**代码#2 :**

```
# Python program explaining 
# numpy.legline() method  

# importing numpy as np   
# and numpy.polynomial.legendre module as geek  
import numpy as np  
import numpy.polynomial.legendre as geek 

# using np.legline() method  
res = geek.legline(1, 4)  

# Resulting legendre series 
print (res)
```

**Output:**

```
[1 4]

```