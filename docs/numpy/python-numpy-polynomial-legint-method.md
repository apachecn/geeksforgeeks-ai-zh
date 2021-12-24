# Python | Numpy 多项式 legint()方法

> 原文:[https://www . geesforgeks . org/python-numpy-多项式-legint-method/](https://www.geeksforgeeks.org/python-numpy-polynomial-legint-method/)

`**np.legint()**`方法用于整合一个**勒让德系列**。

> **语法:** `np.legint(c, m=1, k=[], lbnd=0, scl=1, axis=0)`
> **参数:**
> **c:**【Array _ like】勒让德级数系数数组。
> **m:**【int】积分的顺序，必须为正。默认值为 1。
> **k :** [[]，列表，标量]积分常数。lbnd 处的第一个积分的值是列表中的第一个值，lbnd 处的第二个积分的值是第二个值，等等。如果 k == [](默认值)，所有常量都设置为零。
> **lband :** 【标量，可选】积分的下界。默认值为 0。
> **scl :** 【标量，可选】每次积分，在积分常数相加之前，将结果乘以 scl。默认值为 1。
> **轴:**【标量，可选】取积分的轴。默认值为 0。
> 
> **返回:**【ndarray】积分的勒让德级数系数数组。

**代码#1 :**

```py
# Python program explaining 
# numpy.legint() method  

# importing numpy as np   
# and numpy.polynomial.legendre module as geek  
import numpy as np  
import numpy.polynomial.legendre as geek 

# Legendre series coefficients 

s1 = (2, 4, 8)  

# using np.legint() method  
res = geek.legint(s1)  

# Resulting legendre series 
print (res)  
```

**Output:**

```py
[ 0.66666667  0.4         1.33333333  1.6       ]

```

**代码#2 :**

```py
# Python program explaining 
# numpy.legint() method  

# importing numpy as np   
# and numpy.polynomial.legendre module as geek  
import numpy as np  
import numpy.polynomial.legendre as geek 

# Legendre series coefficients 

s1 = (10, 20, 30, 40, 50)  

# using np.legint() method  
res = geek.legint(s1)  

# Resulting legendre series 
print (res)
```

**Output:**

```py
[-1.66666667  4\.          0.95238095  0.44444444  5.71428571  5.55555556]

```