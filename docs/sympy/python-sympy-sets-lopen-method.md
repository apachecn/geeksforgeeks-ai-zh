# Python | sympy . set . lopen()方法

> 原文:[https://www . geesforgeks . org/python-sympy-set-lopen-method/](https://www.geeksforgeeks.org/python-sympy-sets-lopen-method/)

借助`**sympy.sets.Lopen()**`方法，我们可以通过设置间隔值来制作一组值，如左开，这意味着一组使用`sympy.sets.Lopen()`方法有左开括号和右闭括号。

> **语法:** `sympy.sets.Lopen(val1, val2)`
> **返回:**返回左开集的值集。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.sets.Lopen()`方法，我们能够通过定义左方括号来找到值集。

```
# import sympy
from sympy.sets import Interval

# Use sympy.sets.Lopen() method
gfg = Interval.Lopen(0, 10)
print(gfg)

print(gfg.contains(8))
```

**输出:**

> (0，10]
> 真

**例 2 :**

```
# import sympy
from sympy.sets import Interval

# Use sympy.sets.Lopen() method
gfg = Interval.Lopen(0, 3)
print(gfg)

print(gfg.contains(0))
```

> (0，3]
> 假