# Python | Numpy np.leggauss()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-leggauss-method/](https://www.geeksforgeeks.org/python-numpy-np-leggauss-method/)

`**np.leggauss()**`计算高斯-勒让德求积的样本点和权重。这些样本点和权重将在区间`[-1, 1]`上正确地将次数`2*deg - 1` 或更少的多项式与权重函数`f(x) = 1`积分

> **语法:** `np.leggauss(deg)`
> **参数:**
> **deg:**【int】样本点数量和权重。肯定是> = 1。
> 
> **返回:** 1。包含样本点的一维数组。
> 2。包含权重的一维数组。

**代码#1 :**

```py
# Python program explaining
# numpy.leggauss() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Input degree = 2

degree = 2 

# using np.leggauss() method 
res = geek.leggauss(degree) 

# Resulting array of sample point and weight
print (res) 
```

**Output:**

```py
(array([-0.57735027,  0.57735027]), array([ 1.,  1.]))

```

**代码#2 :**

```py
# Python program explaining
# numpy.leggauss() method 

# importing numpy as np  
# and numpy.polynomial.legendre module as geek 
import numpy as np 
import numpy.polynomial.legendre as geek

# Input degree
degree = 3

# using np.leggauss() method 
res = geek.leggauss(degree) 

# Resulting array of sample point and weight
print (res) 
```

**Output:**

```py
(array([-0.77459667,  0.,  0.77459667]), array([ 0.55555556,  0.88888889,  0.55555556]))

```