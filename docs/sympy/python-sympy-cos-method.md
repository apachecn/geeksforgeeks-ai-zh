# Python | sympy.cos()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-cos-method/](https://www.geeksforgeeks.org/python-sympy-cos-method/)

简单来说，`cos()`方法是余弦函数。利用 simpy 模块中的`cos(x)`方法，可以计算出 x 的余弦值。

```
Syntax : sympy.cos(x)

Return : Returns the cosine of x 
```

**代码#1:**
下面是用 cos()方法求余弦函数的例子。

```
# importing sympy library
from sympy import *

# calling cos() method on expression
geek1 = cos(-1)
geek2 = cos(pi / 3)

print(geek1)
print(geek2)
```

**输出:**

```
cos(1)
1/2

```

**代码#2:**

```
# importing sympy library
from sympy import *

# calling cos() method on expression
geek = cos(2 + 5j)
print(geek)
```

**输出:**

```
-30.8822353189167 - 67.4727884405875*I
```