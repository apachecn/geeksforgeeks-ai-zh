# python 中的 numpy . polysub()

> 原文:[https://www.geeksforgeeks.org/numpy-polysub-in-python/](https://www.geeksforgeeks.org/numpy-polysub-in-python/)

**numpy.polysub()** :这个函数有助于找到两个多项式的差，然后将结果作为多项式返回。每个输入多项式必须是多项式系数序列，从最高到最低。

```py
Parameters : 
p1 : Input polynomial 1 :  1x + 2.
p2 : Input polynomial 2 :  9x2 + 5x + 4

```

**返回:**

```py
Difference of polynomials :  (0-9)x2 + (1-5)x + (2-4)
```

```py
# Python code explaining 
# numpy.polysub ()

# importing libraries
import numpy as np

p1 = np.poly1d([1, 2])
p2 = np.poly1d([9, 5, 4])

print ("P1 : ", p1)
print ("\nP2 : \n", p2)

a = np.polysub(p1, p2)

print ("\nP1 - P2 : \n", a)
```

**输出:**

```py
P1 :   
1 x + 2

P2 : 
    2
9 x + 5 x + 4

P1 - P2 : 
     2
-9 x - 4 x - 2
```