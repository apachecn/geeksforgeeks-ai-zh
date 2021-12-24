# Python | sympy . combinatic .多面体()方法

> 原文:[https://www . geesforgeks . org/python-sympy-combinatic-多面体-method/](https://www.geeksforgeeks.org/python-sympy-combinatoric-polyhedron-method/)

借助**sympy . combinatic .多面体()**方法，通过使用 sympy . combinatic .多面体()方法传递其中的字符列表，可以得到多面体的值。

> **语法:**
> sympy . combinary .多面体()
> **Return:**
> 返回多面体的值。

**示例#1:**

在这个例子中，我们可以看到，通过使用 sympy . combinoric .多面体()方法，我们可以通过传递 list 作为参数来获得多面体的值。

## 蟒蛇 3

```
# import sympy and Polyhedron
from sympy.combinatorics import Polyhedron
from sympy.abc import a, b, c, d, e

# Using sympy.combinatorics.Polyhedron method
gfg = Polyhedron(list('abdce'))

print(gfg)
```

**输出:**

> 多面体((a，b，d，c，e)，()，()

**例 2:**

## 蟒蛇 3

```
# import sympy and Polyhedron
from sympy.combinatorics import Polyhedron

# Using sympy.combinatorics.Polyhedron method
gfg = Polyhedron([[1, 2, 3], [4, 5, 6]])

print(gfg)
```

**输出:**

> 多面体(([1，2，3]，[4，5，6])，()，())