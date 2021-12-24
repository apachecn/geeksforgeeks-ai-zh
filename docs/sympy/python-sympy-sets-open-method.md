# Python | sympy . set . open()方法

> 原文:[https://www . geesforgeks . org/python-sympy-set-open-method/](https://www.geeksforgeeks.org/python-sympy-sets-open-method/)

借助`**sympy.sets.open()**`方法，我们可以通过设置右开或左开这样的区间值来制作一组值，这意味着一个集合使用`sympy.sets.open()`方法有右开括号和左开括号。

> **语法:** `sympy.sets.open(val1, val2)`
> **返回:**左右开集返回一组值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.sets.open()`方法，我们能够通过定义左右开括号来找到值集。

```
# import sympy
from sympy.sets import Interval

# Use sympy.sets.open() method
gfg = Interval.open(0, 10)
print(gfg)

print(gfg.contains(0))
```

**输出:**

> (0，10)
> 假

**例 2 :**

```
# import sympy
from sympy.sets import Interval

# Use sympy.sets.open() method
gfg = Interval.open(0, 5)
print(gfg)

print(gfg.contains(4))
```

> (0，5)
> 真