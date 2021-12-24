# Python | sympy.tan()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-tan-method/](https://www.geeksforgeeks.org/python-sympy-tan-method/)

在 simpy 中，tan()方法是一个正切函数。使用 simpy 模块中的 tan(x)方法，我们可以计算 x 的切线或反正切

```py
Syntax : sympy.tan(x)

Return : Returns the tangent of x 
```

**代码#1:**
下面是用 tan()方法求反正切函数的例子。

## 蟒蛇 3

```py
# importing sympy library
from sympy import *

# calling tan() method on expression
geek1 = tan(-1)
geek2 = tan(pi / 3)

print(geek1)
print(geek2)
```

**输出:**

```py
-tan(1)
sqrt(3)
```

**代码#2:**

## 蟒蛇 3

```py
# importing sympy library
from sympy import tan

# calling tan() method on expression
geek = tan(2 + 5j)
print(geek)
```

**输出:**

```py
-6.87216388011928e-5 + 1.000059350149*I
```