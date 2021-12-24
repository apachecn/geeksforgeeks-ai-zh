# Python | sympy.atan2()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-atan2-method/](https://www.geeksforgeeks.org/python-sympy-atan2-method/)

简单来说，`atan2()`方法是一个反正切函数。使用 simpy 模块中的`atan2(x, y)`方法，我们可以计算双参数反正切。该函数仅针对实数 x 和 y 定义。

```
Syntax : sympy.atan(x)

Return : Returns the arc tangent of x 
```

**代码#1:**
下面是用 atan()方法求逆 tangenet 函数的例子。

```
# importing sympy library
from sympy import *

# calling atan2() method on expression
geek1 = atan2(1, 1)
geek2 = atan2(1, -1)

print(geek1)
print(geek2)
```

**输出:**

```
pi/4
3*pi/4

```

**代码#2:**

```
# importing sympy library
from sympy import atan2

# calling atan2() method on expression
geek = atan2(-1, -1)
print(geek)
```

**输出:**

```
-3*pi/4
```