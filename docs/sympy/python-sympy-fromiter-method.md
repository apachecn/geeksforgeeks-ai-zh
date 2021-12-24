# Python | sympy.fromiter()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-fromiter-method/](https://www.geeksforgeeks.org/python-sympy-fromiter-method/)

借助`**sympy.fromiter()**`方法，我们可以迭代循环，并且可以使用`sympy.fromiter()`方法在元组和列表中添加元素。

> **语法:** `sympy.fromiter()`
> **返回:**返回迭代的元素。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.fromiter()`方法，我们能够迭代循环，并且能够在元组和列表中添加元素。

```
# import sympy
from sympy import *

# Use sympy.fromiter() method
gfg = Tuple.fromiter(i for i in range(6))

print(gfg)
```

**输出:**

> (0, 1, 2, 3, 4, 5)

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.fromiter() method
gfg = List.fromiter(i for i in range(10))

print(gfg)
```

**输出:**

> [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]