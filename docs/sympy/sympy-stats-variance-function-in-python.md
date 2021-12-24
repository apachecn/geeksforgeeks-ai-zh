# Python 中的 sympy . stats . variation()函数

> 原文:[https://www . geesforgeks . org/sympy-stats-variation-function-in-python/](https://www.geeksforgeeks.org/sympy-stats-variance-function-in-python/)

在数学中，方差是检查实际值和任何随机输入之间差异的方法，即方差可以计算为这两个值的平方差。借助`**sympy.stats.variance()**`方法，我们可以用这种方法计算方差的值。

> **语法:** `sympy.stats.variance(value)`
> 
> **返回:**返回方差的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`sympy.stats.variance()`方法，我们能够使用这个方法来计算方差的值。

```py
# Import Sympy and variance
from sympy.stats import P, variance, Die

X, Y = Die('X', 5), Die('Y', 3)

# Using stats.variance() method
gfg = variance(X + Y)

print(gfg)
```

**输出:**

```py
8/3

```

**例 2 :**

```py
# Import Sympy and variance
from sympy.stats import P, variance, Die

X, Y = Die('X', 2), Die('Y', 4)

# Using stats.variance() method
gfg = variance(X * Y)

print(gfg)
```

**输出:**

```py
75/16

```