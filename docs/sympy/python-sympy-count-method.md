# Python | sympy.count()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-count-method/](https://www.geeksforgeeks.org/python-sympy-count-method/)

使用 simpy 模块中的`count()`方法，我们可以统计数学函数中使用的变量数量。`count()`方法返回数学函数中使用的变量数量。

```
Syntax : sympy.count(x)

Return : the count of variables.
```

**代码#1:**

借助下面的例子，我们可以清楚地理解，使用`sympy.count()`方法，我们可以统计给定表达式中的变量数量。

```
# importing sympy library
from sympy import *

# taking symbols
x, y, z = symbols('x y z')

# calling count() method on expression
geek = sqrt((x + 1)**2 + x).count(x)
print(geek)
```

**输出:**

```
2
```

**代码#2:**

```
# importing sympy library
from sympy import *

# taking symbols
a, b = symbols('a b')

# calling count() method on expression
geek = (log(a) + log(b) + log(a)*log(1 / b)).count(b)
print(geek)
```

**输出:**

```
2
```

**代码#3:**

```
# importing sympy library
from sympy import *

# taking symbols
a, b = symbols('a b')

# calling count() method on expression
geek = (log(a * b**(1 - log(a)))).count(b)
print(geek)
```

**输出:**

```
1
```