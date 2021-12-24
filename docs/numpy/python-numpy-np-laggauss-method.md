# Python | Numpy np.laggauss()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag gaus-method/](https://www.geeksforgeeks.org/python-numpy-np-laggauss-method/)

`**np.laggauss()**`计算高斯-拉盖尔求积的样本点和权重。这些样本点和权重将在区间`[0, inf]`上正确地将次数`2*deg - 1` 或更少的多项式与权重函数`f(x) = exp(-x)`积分

> **语法:** `np.laggauss(deg)`
> **参数:**
> **deg:**【int】样本点数量和权重。肯定是> = 1。
> 
> **返回:** 1。包含样本点的一维数组。
> 2。包含权重的一维数组。

**代码#1 :**

```
# Python program explaining
# numpy.laggauss() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Input degree = 2

degree = 2 

# using np.laggauss() method 
res = geek.laggauss(degree) 

# Resulting array of sample point and weight
print (res) 
```

**Output:**

```
(array([ 0.58578644,  3.41421356]), array([ 0.85355339,  0.14644661]))

```

**代码#2 :**

```
# Python program explaining
# numpy.laggauss() method 

# importing numpy as np  
# and numpy.polynomial.laguerre module as geek 
import numpy as np 
import numpy.polynomial.laguerre as geek

# Input degree
degree = 3

# using np.laggauss() method 
res = geek.laggauss(degree) 

# Resulting array of sample point and weight
print (res) 
```

**Output:**

```
(array([ 0.41577456,  2.29428036,  6.28994508]), array([ 0.71109301,  0.27851773,  0.01038926]))

```