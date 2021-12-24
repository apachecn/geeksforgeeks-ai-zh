# Python | sympy . ntherory . prime test . is _ square()方法

> 原文:[https://www . geesforgeks . org/python-sympy-n theory-prime test-is _ square-method/](https://www.geeksforgeeks.org/python-sympy-ntheory-primetest-is_square-method/)

借助`**sympy.ntheory.primetest.is_square()**`方法，我们可以发现在`sympy.ilcm()`方法中作为参数传递的整数是否为完美平方，并返回一个布尔值。

> **语法:** `sympy.ntheory.primetest.is_square(val)`
> **返回:**返回布尔值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.ntheory.primetest.is_square()`方法，我们能够发现作为参数传递的整数是否为完美平方。

```
# import sympy
from sympy.ntheory.primetest import is_square

# Using sympy.ntheory.primetest.is_square() method
gfg = is_square(16)

print(gfg)
```

**输出:**

```
True

```

**例 2 :**

```
# import sympy
from sympy.ntheory.primetest import is_square

# Using sympy.ntheory.primetest.is_square() method
gfg = is_square(24)

print(gfg)
```

**输出:**

```
False

```