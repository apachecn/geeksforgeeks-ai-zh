# Python | sympy.acot()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-acot-method/](https://www.geeksforgeeks.org/python-sympy-acot-method/)

借助`**sympy.acot()**`方法，我们可以利用`sympy.acot()`函数求出 cot 逆的值。

> **语法:** `sympy.acot()`
> **返回:**cot 逆的返回值。

**例#1 :**
在这个例子中我们可以看到，通过使用`sympy.acot()`方法，我们可以找到 cot 逆的值。

```py
# import sympy
from sympy import *

# Use sympy.acot() method
gfg = simplify(acot(0.3))

print(gfg)
```

**输出:**

> 1.27933953231703

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.acot() method
gfg = simplify(acot(0.5))

print(gfg)
```

**输出:**

> 1.10714871779409