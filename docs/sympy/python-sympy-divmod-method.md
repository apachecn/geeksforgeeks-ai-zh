# Python | sympy.divmod()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-divmod-method/](https://www.geeksforgeeks.org/python-sympy-divmod-method/)

借助`sympy.divmod()`方法，我们可以求出给定值的模和商。

```
 Syntax: sympy.divmod(val1, val2)

 Return: (quotient, modulo)

```

**示例#1 :**

```
# import sympy 
from sympy import *

# Using sympy.divmod() method 
gfg = divmod(Integer(48), Integer(7))

print(gfg)
```

**输出:**

```
(6, 6)
```

**示例#2 :**

```
# import sympy 
from sympy import *

# Using sympy.divmod() method 
gfg = divmod(48.2, Integer(7))

print(gfg)
```

**输出:**

```
(6, 6.2)
```