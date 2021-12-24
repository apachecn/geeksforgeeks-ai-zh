# Python | sympy.bernoulli()方法

> 原文:[https://www . geesforgeks . org/python-sympy-Bernoulli-method/](https://www.geeksforgeeks.org/python-sympy-bernoulli-method/)

借助**辛.伯努利()**方法，我们可以在辛中找到[伯努利数](https://en.wikipedia.org/wiki/Bernoulli_number)和[伯努利多项式](https://en.wikipedia.org/wiki/Bernoulli_polynomial)。

### `bernoulli(n) -`

> **语法:**伯努利(n)
> 
> **参数:**
> **n–**表示第 n 个伯努利数。
> 
> **返回:**返回第 n 个<sup>伯努利数。</sup>

**示例#1:**

```py
# import sympy 
from sympy import * n = 4
print("Value of n = {}".format(n))

# Use sympy.bernoulli() method 
nth_bernoulli = bernoulli(n)  

print("Value of nth bernoulli number : {}".format(nth_bernoulli))  
```

**输出:**

```py
Value of n = 4
Value of nth bernoulli number : -1/30

```

### `bernoulli(n, k) -`

> **语法:**伯努利(n，k)
> 
> **参数:**
> **n–**它表示伯努利多项式的阶。
> **k–**表示伯努利多项式中的变量。
> 
> **返回:**返回伯努利多项式的表达式或其值。

**例 2:**

```py
# import sympy 
from sympy import * n = 5
k = symbols('x')
print("Value of n = {} and k = {}".format(n, k))

# Use sympy.bernoulli() method 
nth_bernoulli_poly = bernoulli(n, k)  

print("The nth bernoulli polynomial : {}".format(nth_bernoulli_poly))  
```

**输出:**

```py
Value of n = 5 and k = x
The nth bernoulli polynomial : x**5 - 5*x**4/2 + 5*x**3/3 - x/6

```

**示例#3:**

```py
# import sympy 
from sympy import * n = 4
k = 3
print("Value of n = {} and k = {}".format(n, k))

# Use sympy.bernoulli() method 
nth_bernoulli_poly = bernoulli(n, k)  

print("The nth bernoulli polynomial value : {}".format(nth_bell_poly))  
```

**输出:**

```py
Value of n = 4 and k = 3
The nth bernoulli polynomial value : 10*x1**2*x3 + 15*x1*x2**2

```