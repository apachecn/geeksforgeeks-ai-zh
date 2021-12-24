# 如何用 Python 中的 NumPy 将一个多项式分解成另一个多项式？

> 原文:[https://www . geeksforgeeks . org/如何使用 python 中的 numpy 将一个多项式除以另一个多项式/](https://www.geeksforgeeks.org/how-to-divide-a-polynomial-to-another-using-numpy-in-python/)

在本文中，我们将制作一个 [NumPy](https://www.geeksforgeeks.org/python-numpy/) 程序来将一个多项式划分为另一个多项式。给出两个多项式作为输入，结果是除法的商和余数。

*   多项式 **p(x) = C3 x2 + C2 x + C1** 在 NumPy 中表示为: **( C1、C2、C3 )** {系数(常数)}。
*   让我们取两个多项式 p(x)和 g(x)，然后除以它们，得到商 q(x) = p(x) // g(x)和余数 r(x) = p(x) % g(x)。

```
If p(x) = A3 x2 + A2 x + A1
and 
g(x) = B3 x2 + B2 x + B1 

then result is 
q(x) = p(x) // g(x) and r(x) = p(x) % g(x)

and the output is coefficientes of remainder and
 the coefficientes of quotient.

```

这可以使用[聚二夫()](https://www.geeksforgeeks.org/numpy-polydiv-in-python/)方法计算。这个方法计算两个多项式的除法，并返回多项式除法的商和余数。

**语法:**

```
numpy.polydiv(p1, p2)
```

下面是一些示例的实现:

**例 1 :**

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = 5(x**2) + (-2)x +5
px = (5, -2, 5)

# g(x) = x +2
gx = (2, 1, 0)

# divide the polynomials
qx, rx = numpy.polynomial.polynomial.polydiv(px, gx)

# print the result
# quotiient
print(qx)

# remainder
print(rx)
```

**输出:**

```
[-12\.   5.]
[ 29.]
```

**例 2 :**

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = (x**2) + 3x + 2
px = (1,3,2)

# g(x) = x + 1
gx = (1,1,0)

# divide the polynomials
qx,rx = numpy.polynomial.polynomial.polydiv(px,gx)

# print the result
# quotiient
print(qx)

# remainder
print(rx)
```

**输出:**

```
[ 1\.  2.]
[ 0.]

```