# Python | sympy . set . Ropen()方法

> 原文:[https://www . geesforgeks . org/python-sympy-set-ropen-method/](https://www.geeksforgeeks.org/python-sympy-sets-ropen-method/)

借助`**sympy.sets.Ropen()**`方法，我们可以通过设置区间值来制作一组值，如右开，即使用`sympy.sets.Ropen()`方法设置一组有右开括号和左闭括号。

> **语法:** `sympy.sets.Ropen(val1, val2)`
> **返回:**用右开集返回一组值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.sets.Ropen()`方法，我们能够通过定义右开括号来找到值集。

```py
# import sympy
from sympy.sets import Interval

# Use sympy.sets.Ropen() method
gfg = Interval.Ropen(0, 10)
print(gfg)

print(gfg.contains(0))
```

**输出:**

> [0，10)
> 真

**例 2 :**

```py
# import sympy
from sympy.sets import Interval

# Use sympy.sets.Ropen() method
gfg = Interval.Ropen(0, 5)
print(gfg)

print(gfg.contains(5))
```

> [0，5)
> 假