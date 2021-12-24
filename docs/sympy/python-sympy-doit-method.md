# python | sympty . debt()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-sympty-owe-method/

使用 simpy 模块中的`doit()`方法，我们可以评估默认不评估的对象，如极限、积分、求和和乘积。请注意，所有这类对象都将被递归计算。

```
Syntax : sympy.doit(x)

Return : evaluated object 
```

**代码#1:**

借助下面的例子，我们可以清楚地理解，使用`sympy.doit()`方法，我们可以评估默认不评估的对象。

```
# importing sympy library
from sympy import * from sympy.abc import x

# calling doit() method on expression
geek = (2 * Integral(x, x)).doit()

print(geek)
```

**输出:**

```
x**2
```

**代码#2:**

```
# importing sympy library
from sympy import *

# taking symbols
a, b = symbols('a b')

# calling doit() method on expression
geek = (3 * a + b * log(a) + log(b) + log(a)*log(1 / b)).doit()
print(geek)
```

**输出:**

```
3*a + b*log(a) + log(a)*log(1/b) + log(b)
```