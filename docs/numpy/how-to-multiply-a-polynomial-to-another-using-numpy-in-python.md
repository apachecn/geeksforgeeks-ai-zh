# 如何用 Python 中的 NumPy 将一个多项式乘以另一个多项式？

> 原文:[https://www . geeksforgeeks . org/如何使用 python 中的 numpy 将一个多项式乘以另一个多项式/](https://www.geeksforgeeks.org/how-to-multiply-a-polynomial-to-another-using-numpy-in-python/)

在本文中，我们将制作一个 [NumPy](https://www.geeksforgeeks.org/python-numpy/) 程序来将一个多项式相乘。给出两个多项式作为输入，结果是两个多项式的乘积。

*   多项式 **p(x) = C3 x2 + C2 x + C1** 在 NumPy 中表示为: **( C1、C2、C3 )** {系数(常数)}。
*   让我们取两个多项式 p(x)和 q(x)，然后将它们相乘，得到 r(x) = p(x) * q(x)作为两个输入多项式相乘的结果。

```
If p(x) = A3 x2 + A2 x + A1 
and 
q(x) = B3 x2 + B2 x + B1 

then result is r(x) = p(x) * q(x) 

and output is 

( (A1 * B1), (A2 * B1) + (A2 * B1),
(A3 * B1) + (A2 * B2) + (A1 * B3), 
(A2 * B2) + (A3 * B2), (A3 * B3) ).

```

这可以使用 NumPy 的 [polymul()](https://www.geeksforgeeks.org/numpy-polymul-in-python/) 方法来计算。这个方法计算两个多项式的乘积，并返回两个输入多项式‘P1’和‘p2’相乘得到的多项式。

**语法:**

```
numpy.polymul(p1, p2)
```

下面是一些示例的实现:

**例 1:**

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = 5(x**2) + (-2)x +5

px = (5, -2, 5)
# q(x) = 2(x**2) + (-5)x +2
qx = (2, -5, 2)

# mul the polynomials
rx = numpy.polynomial.polynomial.polymul(px, qx)

# print the resultant polynomial
print(rx)
```

**输出:**

```
[ 10\. -29\.  30\. -29\.  10.] 

```

**例 2 :**

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = 2.2
px = (0, 0, 2.2)

# q(x) = 9.8(x**2) + 4
qx = (9.8, 0, 4)

# mul the polynomials
rx = numpy.polynomial.polynomial.polymul(px, qx)

# print the resultant polynomial
print(rx)
```

**输出:**

```
[  0\.     0\.    21.56   0\.     8.8 ]

```

**例 3 :**

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = (5/3)x
px = (0, 5/3, 0)

# q(x) = (-7/4)(x**2) + (9/5)
qx = (-7/4, 0, 9/5)

# mul the polynomials
rx = numpy.polynomial.polynomial.polymul(px, qx)

# print the resultant polynomial
print(rx)
```

**输出:**

```
[ 0\.         -2.91666667  0\.          3\.        ]

```