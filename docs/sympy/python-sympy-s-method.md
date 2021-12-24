# Python | sympy。s()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-s-method/](https://www.geeksforgeeks.org/python-sympy-s-method/)

借助`**sympy.S()**`方法，我们可以使用`sympy.S()`方法制作一个对象的单个实例，其中 S 表示单例类。

> **语法:** `sympy.S()`
> **返回:**返回一个对象的单个实例。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.S()`方法，我们能够创建任何对象的单个实例。

```py
# import sympy
from sympy import *

# Use sympy.S() method
gfg = Integer(0)

print(gfg == S.Zero)
```

**输出:**

> 真实的

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.S() method
gfg = Rational(1, 2)

print(gfg == S.Half)
```

**输出:**

> 真实的