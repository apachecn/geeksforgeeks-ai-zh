# 如何用 Python 中的 NumPy 将一个多项式加到另一个多项式上？

> 原文:[https://www . geeksforgeeks . org/如何使用 python 中的 numpy 将一个多项式与另一个多项式相加/](https://www.geeksforgeeks.org/how-to-add-one-polynomial-to-another-using-numpy-in-python/)

在本文中，让我们看看如何将一个多项式添加到另一个多项式中。给出两个多项式作为输入，结果是两个多项式的相加。

*   多项式**p(x)= C<sub>3</sub>x<sup>2</sup>+C<sub>2</sub>x+C<sub>1</sub>**在 NumPy 中表示为: **( C1、C2、C3 )** {系数(常数)}。
*   让我们取两个多项式 p(x)和 q(x)，然后相加得到 r(x) = p(x) + q(x)，这是两个输入多项式相加的结果。

```
If p(x) = A3 x2 + A2 x + A1 
and
q(x) = B3 x2 + B2 x + B1 

then result is 
r(x) = p(x) + q(x) 
i.e;
r(x) = (A3 + B3) x2 + (A2 + B2) x + (A1 + B1)

and output is 
( (A1 + B1), (A2 + B2), (A3 + B3) )

```

下面是一些示例的实现:

**示例 1:** 简单易用

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = 5(x**2) + (-2)x +5
px = (5,-2,5)

# q(x) = 2(x**2) + (-5)x +2
qx = (2,-5,2)

# add the polynomials
rx = numpy.polynomial.polynomial.polyadd(px,qx)

# print the resultant polynomial
print(rx)
```

**输出:**

```
[ 7\. -7\.  7.]

```

**例 2:** #add_with_decimals

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = 2.2
px = (0,0,2.2)

# q(x) = 9.8(x**2) + 4
qx = (9.8,0,4)

# add the polynomials
rx = numpy.polynomial.polynomial.polyadd(px,qx)

# print the resultant polynomial
print(rx)
```

**输出:**

```
[ 9.8  0\.   6.2]

```

**示例 3:** eval_then_add

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = (5/3)x
px = (0,5/3,0)

# q(x) = (-7/4)(x**2) + (9/5)
qx = (-7/4,0,9/5)

# add the polynomials
rx = numpy.polynomial.polynomial.polyadd(px,qx)

# print the resultant polynomial
print(rx)
```

**输出:**

```
[-1.75        1.66666667  1.8       ]

```