# 如何用 Python 中的 NumPy 将一个多项式减去另一个多项式？

> 原文:[https://www . geeksforgeeks . org/如何使用 python 中的 numpy 将一个多项式减去另一个多项式/](https://www.geeksforgeeks.org/how-to-subtract-one-polynomial-to-another-using-numpy-in-python/)

在这篇文章中，让我们讨论如何将一个多项式减去另一个多项式。给出两个多项式作为输入，结果是两个多项式的相减。

*   多项式 **p(x) = C3 x2 + C2 x + C1** 在 NumPy 中表示为: **( C1、C2、C3 )** {系数(常数)}。
*   让我们取两个多项式 p(x)和 q(x)，然后减去它们，得到 r(x)= p(x)–q(x)，这是两个输入多项式相减的结果。

```
If p(x) = A3 x2 + A2 x + A1 
and
q(x) = B3 x2 + B2 x + B1 

then result is 
r(x) = p(x) - q(x) i.e;
r(x) = (A3 - B3) x2 + (A2 - B2) x + (A1 - B1) 

and output is 
( (A1 - B1), (A2 - B2), (A3 - B3) ).

```

在 NumPy 中，可以使用 [polysub()](https://www.geeksforgeeks.org/numpy-polysub-in-python/) 方法求解。该函数有助于找到两个多项式的差，然后将结果作为多项式返回

下面是一些示例的实现:

**示例 1:** 使用[多边形()](https://www.geeksforgeeks.org/numpy-polysub-in-python/)

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = 5(x**2) + (-2)x +5
px = (5,-2,5)

# q(x) = 2(x**2) + (-5)x +2
qx = (2,-5,2)

# subtract the polynomials
rx = numpy.polynomial.polynomial.polysub(px,qx)

# print the resultant polynomial
print(rx)
```

**输出:**

```
[ 3\.  3\.  3.]
```

**示例 2:** 带 _ 小数的子

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = 2.2
px = (0,0,2.2)

# q(x) = 9.8(x**2) + 4
qx = (9.8,0,4)

# subtract the polynomials
rx = numpy.polynomial.polynomial.polysub(px,qx)

# print the resultant polynomial
print(rx)
```

**输出:**

```
[-9.8  0\.  -1.8]

```

**示例 3:** #eval_then_sub

## 蟒蛇 3

```
# importing package
import numpy

# define the polynomials
# p(x) = (5/3)x
px = (0,5/3,0)

# q(x) = (-7/4)(x**2) + (9/5)
qx = (-7/4,0,9/5)

# subtract the polynomials
rx = numpy.polynomial.polynomial.polysub(px,qx)

# print the resultant polynomial
print(rx)
```

**输出:**

```
[ 1.75        1.66666667 -1.8       ]       

```