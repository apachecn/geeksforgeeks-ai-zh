# Python | sympy。间隔()。包含()方法

> 原文:[https://www . geesforgeks . org/python-sympy-interval-contains-method/](https://www.geeksforgeeks.org/python-sympy-interval-contains-method/)

借助**方法，我们可以使用`sympy.Interval().contains()`方法检查区间中是否存在某个值。**

> ****语法:** `sympy.Interval(x, y).contains(value)`**
> 
> ****返回:**返回布尔值真或假。**

****示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.Interval().contains()`方法，我们能够获得布尔值，无论值是否出现在区间中。**

```
# import sympy, Interval
from sympy import Interval

# Using sympy.Interval().contains() method
gfg = Interval(5, 10).contains(7)

print(gfg)
```

****输出:****

> **真实的**

****例 2 :****

```
# import sympy, Interval
from sympy import Interval

# Using sympy.Interval().contains() method
gfg = Interval(0, 1).contains(1.5)

print(gfg)
```

****输出:****

> **错误的**