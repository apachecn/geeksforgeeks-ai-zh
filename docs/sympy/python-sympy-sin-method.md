# Python | symy . sin()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-sin-method/](https://www.geeksforgeeks.org/python-sympy-sin-method/)

简单来说，`sin()`方法是正弦函数。利用 simpy 模块中的`sin(x)`方法，可以计算出 x 的正弦值。

```py
Syntax : sympy.sin(x)
Return : Returns the sine of x 
```

**代码#1:**
下面是用 sin()方法求正弦函数的例子。

```py
# importing sympy library
from sympy import *

# calling sin() method on expression
geek1 = sin(-1)
geek2 = sin(pi / 3)

print(geek1)
print(geek2)
```

**输出:**

```py
-sin(1)
sqrt(3)/2

```

**代码#2:**

```py
# importing sympy library
from sympy import *

# calling sin() method on expression
geek = sin(2 + 5j)
print(geek)
```

**输出:**

```py
67.4789152384559 - 30.8794313435882*I

```