# Python 中的 numpy.poly1d()

> 原文:[https://www.geeksforgeeks.org/numpy-poly1d-in-python/](https://www.geeksforgeeks.org/numpy-poly1d-in-python/)

**numpy.poly1d()** 函数有助于定义多项式函数。它使得对多项式应用“自然运算”变得容易。

> **语法:** numpy.poly1d(arr，root，var)
> **参数:**
> **arr:**【array _ like】多项式系数按幂的递减顺序给出。如果第二个参数(根)设置为真，那么数组值就是多项式方程的根。
> 
> **根:**【bool，可选】True 表示多项式根。默认值为假。
> **var :** 我们在多项式中需要的像 x，y，z 这样的变量[默认值是 x]。
> 
> **自变量:**
> **c :** 多项式系数。
> **系数:**多项式系数。
> **系数:**多项式系数。
> **阶数:**多项式的阶数或次数。
> **o :** 多项式的阶或次。
> **r :** 多项式根。
> **根:**多项式根。
> 
> **返回:**多项式和应用的运算

> **例如:** poly1d(3，2，6)= 3x<sup>2</sup>+2x+6
> poly 1d(【1，2，3】，True)=(x-1)(x-2)(x-3)= x<sup>3</sup>–6x<sup>2</sup>+11x-6

**代码 1:解释 poly1d()及其参数**

```py
# Python code explaining
# numpy.poly1d()

# importing libraries
import numpy as np

# Constructing polynomial
p1 = np.poly1d([1, 2])
p2 = np.poly1d([4, 9, 5, 4])

print ("P1 : ", p1)
print ("\n p2 : \n", p2)

# Solve for x = 2
print ("\n\np1 at x = 2 : ", p1(2))
print ("p2 at x = 2 : ", p2(2))

# Finding Roots
print ("\n\nRoots of P1 : ", p1.r)
print ("Roots of P2 : ", p2.r)

# Finding Coefficients
print ("\n\nCoefficients of P1 : ", p1.c)
print ("Coefficients of P2 : ", p2.coeffs)

# Finding Order
print ("\n\nOrder / Degree of P1 : ", p1.o)
print ("Order / Degree of P2 : ", p2.order)
```

**输出:**

```py
P1 :   
1 x + 2

 p2 : 
    3     2
4 x + 9 x + 5 x + 4

p1 at x = 2 :  4
p2 at x = 2 :  82

Roots of P1 :  [-2.]
Roots of P2 :  [-1.86738371+0.j         -0.19130814+0.70633545j -0.19130814-0.70633545j]

Coefficients of P1 :  [1 2]
Coefficients of P2 :  [4 9 5 4]

Order / Degree of P1 :  1
Order / Degree of P2 :  3
```

**代码 2:多项式的基本数学运算**

```py
# Python code explaining
# numpy.poly1d()

# importing libraries
import numpy as np

# Constructing polynomial
p1 = np.poly1d([1, 2])
p2 = np.poly1d([4, 9, 5, 4])

print ("P1 : ", p1)
print ("\n p2 : \n", p2)

print ("\n\np1 ^ 2 : \n", p1**2)
print ("p2 ^ 2 : \n", np.square(p2))

p3 = np.poly1d([1, 2], variable = 'y')
print ("\n\np3 : ", p3)

print ("\n\np1 * p2 : \n", p1 * p2)
print ("\nMultiplying two polynimials : \n", 
       np.poly1d([1, -1]) * np.poly1d([1, -2]))
```

**输出:**

```py
P1 :   
1 x + 2

 p2 : 
    3     2
4 x + 9 x + 5 x + 4

p1 ^ 2 : 
    2
1 x + 4 x + 4
p2 ^ 2 : 
 [16 81 25 16]

p3 :   
1 y + 2

p1 * p2 : 
    4      3      2
4 x + 17 x + 23 x + 14 x + 8

Multiplying two polynimials : 
    2
1 x - 3 x + 2
```