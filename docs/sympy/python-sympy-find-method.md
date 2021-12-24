# Python | sympy.find()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-find-method/](https://www.geeksforgeeks.org/python-sympy-find-method/)

使用 simpy 模块中的`find()`方法，我们可以找到数学函数中的子表达式(如果存在)。`find()`方法返回数学函数中的子表达式。

```
Syntax : sympy.find(x)

Return : returns subexpression 
```

**代码#1:**

借助下面的例子，我们可以清楚地理解，使用`sympy.find()`方法，我们可以从给定的表达式中计算子表达式。

```
# importing sympy library
from sympy import *

# taking symbols
x, y, z = symbols('x y z')

# calling find() method on expression
geek = (3 * x + log(3 * x) + sqrt((x + 1)**2 + x)).find(log)
print(geek)
```

**输出:**

```
set([log(3*x)])
```

**代码#2:**

```
# importing sympy library
from sympy import *

# taking symbols
a, b = symbols('a b')

# calling find() method on expression
geek = (3 * a + b * log(a) + log(b) + log(a)*log(1 / b)).find(log)
print(geek)
```

**输出:**

```
set([log(a), log(1/b), log(b)])
```