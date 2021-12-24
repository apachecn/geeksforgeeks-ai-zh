# Python |开始使用 SymPy 模块

> 原文:[https://www . geeksforgeeks . org/python-入门-sympy-module/](https://www.geeksforgeeks.org/python-getting-started-with-sympy-module/)

[**SymPy**](https://www.scipy-lectures.org/advanced/sympy.html) 是一个符号数学的 Python 库。它的目标是成为一个功能齐全的计算机代数系统(CAS)，同时保持代码尽可能简单，以便易于理解和扩展。SymPy 完全是用 Python 编写的。
SymPy 只依赖于 mpmath，这是一个用于任意浮点运算的纯 Python 库，使用起来很方便。
**安装症状模块:**

```py
 pip install sympy 

```

### 作为计算器:

SymPy 定义了以下数值类型:*有理*和*整数*。有理数类将有理数表示为一对两个整数，分子和分母，所以有理数(1，2)表示 1/2，有理数(5，2)表示 5/2，依此类推。整数类表示整数。
**例 1 :**

## 蟒蛇 3

```py
# import everything from sympy module
from sympy import *

a = Rational(5, 8)
print("value of a is :" + str(a))

b = Integer(3.579)
print("value of b is :" + str(b))
```

**输出:**

```py

value of a is :5/8
value of b is :3

```

SymPy 在后台使用 mpmath，这使得使用任意精度的算法执行计算成为可能。这样，一些特殊的常数，如 exp，pi，oo (Infinity)，被视为符号，可以任意精度计算。
**例 2 :**

## 蟒蛇 3

```py
# import everything from sympy module
from sympy import *

# you can't get any numerical value
p = pi**3
print("value of p is :" + str(p))

# evalf method evaluates the expression to a floating-point number
q = pi.evalf()
print("value of q is :" + str(q))

# equivalent to e ^ 1 or e ** 1
r = exp(1).evalf()
print("value of r is :" + str(r))

s = (pi + exp(1)).evalf()
print("value of s is :" + str(s))

rslt = oo + 10000
print("value of rslt is :" + str(rslt))

if oo > 9999999 :
    print("True")
else:
    print("False")
```

**输出:**

```py
value of p is :pi^3
value of q is :3.14159265358979
value of r is :2.71828182845905
value of s is :5.85987448204884
value of rslt is :oo
True

```

与其他计算机代数系统不同，在 SymPy 中，必须使用 Symbol()方法显式声明符号变量。
**例 3 :**

## 蟒蛇 3

```py
# import everything from sympy module
from sympy import * x = Symbol('x')
y = Symbol('y')

z = (x + y) + (x-y)
print("value of z is :" + str(z))
```

**输出:**

```py
value of z is :2*x 

```

### 微积分:

象 SymPy 这样的符号计算系统的真正力量是象征性地进行各种计算的能力。SymPy 可以简化表达式、计算导数、积分和极限、求解方程、处理矩阵等等，并且可以象征性地完成所有工作。这是 SymPy 能够激发你的食欲的象征性力量的一小部分。
**例 4 :** 求导数、积分、极限、二次方程。

## 蟒蛇 3

```py
# import everything from sympy module
from sympy import *

# make a symbol
x = Symbol('x')

# ake the derivative of sin(x)*e ^ x
ans1 = diff(sin(x)*exp(x), x)
print("derivative of sin(x)*e ^ x : ", ans1)

# Compute (e ^ x * sin(x)+ e ^ x * cos(x))dx
ans2 = integrate(exp(x)*sin(x) + exp(x)*cos(x), x)
print("indefinite integration is : ", ans2)

# Compute definite integral of sin(x ^ 2)dx
# in b / w interval of ? and ?? .
ans3 = integrate(sin(x**2), (x, -oo, oo))
print("definite integration is : ", ans3)

# Find the limit of sin(x) / x given x tends to 0
ans4 = limit(sin(x)/x, x, 0)
print("limit is : ", ans4)

# Solve quadratic equation like, example : x ^ 2?2 = 0
ans5 = solve(x**2 - 2, x)
print("roots are : ", ans5)
```

**输出:**

```py
derivative of sin(x)*e^x :  exp(x)*sin(x) + exp(x)*cos(x)
indefinite integration is :  exp(x)*sin(x)
definite integration is :  sqrt(2)*sqrt(pi)/2
limit is :  1
roots are :  [-sqrt(2), sqrt(2)]

```