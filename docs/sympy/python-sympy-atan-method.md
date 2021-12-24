# Python | sympy.atan()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-atan-method/](https://www.geeksforgeeks.org/python-sympy-atan-method/)

简单来说，atan()方法是一个反正切函数。使用 simpy 模块中的 atan(x)方法，我们可以计算 x 的反正切或反正切

```
Syntax : sympy.atan(x)

Return : Returns the arc tangent of x 
```

**代码#1:**
下面是用 atan()方法求反正切函数的例子。

## 蟒蛇 3

```
# importing sympy library
from sympy import *

# calling atan() method on expression
geek1 = atan(-1)
geek2 = atan(1)

print(geek1)
print(geek2)
```

**输出:**

```
-pi/4
pi/4
```

**代码#2:**

## 蟒蛇 3

```
# importing sympy library
from sympy import atan

# calling atan() method on expression
geek = atan(1)
print(geek)
```

**输出:**

```
pi/4
```