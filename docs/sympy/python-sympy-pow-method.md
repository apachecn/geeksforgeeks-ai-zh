# Python | sympy。Pow()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-pow-method/](https://www.geeksforgeeks.org/python-sympy-pow-method/)

借助**症状。Pow()** 法，我们可以找到 ***a*** 提升到 ***b*** 的力量，其中 ***a*** 和 ***b*** 都是该法的参数。

> **语法:** Pow(a，b)
> **参数:**
> **a–**表示整数。
> **b–**表示整数。
> 
> **返回:**返回一个整数，等于 a 的 b 的幂，即 a^b.

**示例#1:**

```py
# import Pow() method from sympy
from sympy import Pow

a = 3
b = 3

# Use Pow() method 
pow_a_b = Pow(a, b) 

print("{}^{} = {}".format(a, b, pow_a_b))
```

**输出:**

```py
3^3 = 27

```

**例 2:**

```py
# import Pow() method from sympy
from sympy import Pow

a = 5
b = 4

# Use Pow() method 
pow_a_b = Pow(a, b) 

print("{}^{} = {}".format(a, b, pow_a_b))
```

**输出:**

```py
5^4 = 625

```