# Python | sympy.cot()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-cot-method/](https://www.geeksforgeeks.org/python-sympy-cot-method/)

借助`**sympy.cot()**`方法，我们可以利用`sympy.cot()`函数求出 cot 的值。

> **语法:** `sympy.cot()`
> **返回:**cotθ的返回值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.cot()`方法，我们可以找到 cot 的值。

```
# import sympy
from sympy import *

# Use sympy.cot() method
gfg = simplify(cot(pi / 3))

print(gfg)
```

**输出:**

> sqrt(3)/3

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.cot() method
gfg = simplify(cot(pi / 4))

print(gfg)
```

**输出:**

> one