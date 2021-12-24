# Python | sympy.compare()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-compare-method/](https://www.geeksforgeeks.org/python-sympy-compare-method/)

借助`**sympy.compare()**`方法，我们可以比较变量，使用`sympy.compare()`方法，它将返回 3 个值，即-1 表示较小，0 表示相等，1 表示较大。

> **语法:** `sympy.compare()`
> **返回:**返回比较的值即-1，0，1。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.compare()`方法，我们能够比较变量并返回 3 个值，即-1 表示较小，0 表示相等，1 表示较大。

```
# import sympy
from sympy import *
x, y = symbols('x y')

# Use sympy.compare() method
gfg = x.compare(y)

print(gfg)
```

**输出:**

> -1

**例 2 :**

```
# import sympy
from sympy import *
x, y = symbols('x y')

# Use sympy.compare() method
gfg = x.compare(x)

print(gfg)
```

**输出:**

> Zero

**示例#3 :**

```
# import sympy
from sympy import *
x, y = symbols('x y')

# Use sympy.compare() method
gfg = y.compare(x)

print(gfg)
```

**输出:**

> one