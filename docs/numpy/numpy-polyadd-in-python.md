# num py . polydd()在 Python

中

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-polydd-in-python/

**numpy.polyadd() :** 这个函数有助于找到两个多项式的和，然后将结果作为多项式返回。每个输入多项式必须是多项式系数序列，从最高到最低。

**参数:**

```
p1 : Input polynomial 1
p2 : Input polynomial 2

```

**返回:**

```
Sum of polynomials
```

```
# Python code explaining 
# numpy.polyadd ()

# importing libraries
import numpy as np

p1 = np.poly1d([1, 2])
p2 = np.poly1d([9, 5, 4])

print ("P1 : ", p1)
print ("\nP2 : \n", p2)

a = np.polyadd(p1, p2)

print ("\nP1 + P2 : \n", a)
```

**输出:**

```
P1 :   
1 x + 2

P2 : 
    2
9 x + 5 x + 4

P1 + P2 : 
    2
9 x + 6 x + 6
```