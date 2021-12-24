# Python 中的 numpy.polydiv()

> 原文:[https://www.geeksforgeeks.org/numpy-polydiv-in-python/](https://www.geeksforgeeks.org/numpy-polydiv-in-python/)

**numpy . poldiv()**方法计算两个多项式的除法，并返回多项式除法的商和余数。

> **语法:** numpy.polydiv(p1，p2)
> **参数:**
> **P1:**【array _ like 或 poly1D】被除数多项式的系数。
> **p2:**【array _ like 或 poly1D】除数多项式的系数。
> 
> **返回:**
> **q:**【ndarray】商的系数。
> **r:**【n 数组】余数系数。

**代码:解释聚二夫()**的 Python 代码

```
# Python code explaining 
# numpy.polydiv()

# importing libraries
import numpy as np
import pandas as pd

# Constructing polynomial 
p1 = np.poly1d([1, 2]) 
p2 = np.poly1d([4, 9, 5, 4]) 

print ("P1 : ", p1) 
print ("\n p2 : \n", p2) 
```

![](img/ae4c9bc610e029913b2770d0c2c2c9eb.png)

```
quotient, remainder = np.polydiv(p2, p1)

print("\n\nquotient  : ", quotient)
print("remainder : ", remainder)
print ("\n")
```

![](img/25035d3520c97ba746a0f2efa6050715.png)

```
# Defining ndarray
x = np.array([1, 2])
y = np.array([4, 9, 5, 4])

quotient, remainder = np.polydiv(y, x)

print("quotient  : ", quotient)
print("remainder : ", remainder)
```

![](img/f1b7ad58ff3eab9a2ca73b0d4384edcf.png)