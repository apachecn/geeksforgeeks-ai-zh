# Python | sympy.count_ops()方法

> 原文:[https://www . geesforgeks . org/python-sympy-count _ ops-method/](https://www.geeksforgeeks.org/python-sympy-count_ops-method/)

使用 simpy 模块中的`count_ops()`方法，我们可以统计数学函数中使用的运算次数。`count_ops()`方法返回数学函数中使用的运算次数。

```
Syntax : sympy.count_ops()

Return : the count of operations.
```

**代码#1:**

借助下面的例子，我们可以清楚地理解，使用 `sympy.count_ops()`方法可以统计给定表达式中的运算次数。

```
# importing sympy library
from sympy import *

# taking symbols
x, y, z = symbols('x y z')

# calling count_ops() method on expression
geek = sqrt((x + 1)**2 + x).count_ops()
print(geek)
```

**输出:**

```
5
```

**代码#2:**

```
# importing sympy library
from sympy import *

# taking symbols
a, b = symbols('a b')

# calling count_ops() method on expression
geek = log(a) + log(b) + log(a)*log(1 / b)
print(count_ops(geek))
```

**输出:**

```
8
```

**代码#3:**

```
# importing sympy library
from sympy import *

# taking symbols
a, b = symbols('a b')

# calling count_ops() method on expression
geek = log(a * b**(1 - log(a)))
print(count_ops(geek))
```

**输出:**

```
5
```