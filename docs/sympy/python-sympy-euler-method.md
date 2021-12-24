# Python | sympy.euler()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-euler-method/](https://www.geeksforgeeks.org/python-sympy-euler-method/)

借助**辛.欧拉()**方法，我们可以在辛中找到[欧拉数和欧拉多项式](https://en.wikipedia.org/wiki/Euler_numbers)。

### `euler(n) -`

> **语法:**欧拉(n)
> 
> **参数:**
> **n–**表示第 n 个欧拉数。
> 
> **返回:**返回第 n 个<sup>欧拉数。</sup>

**示例#1:**

```py
# import sympy 
from sympy import * n = 4
print("Value of n = {}".format(n))

# Use sympy.euler() method 
nth_euler = euler(n)  

print("Value of nth euler number : {}".format(nth_euler))  
```

**输出:**

```py
Value of n = 4
Value of nth euler number : 5

```

### `euler(n, k) -`

> **语法:**欧拉(n，k)
> 
> **参数:**
> **n–**表示欧拉多项式的阶数。
> **k–**表示欧拉多项式中的变量。
> 
> **返回:**返回欧拉多项式的表达式或其值。

**例 2:**

```py
# import sympy 
from sympy import * n = 5
k = symbols('x')
print("Value of n = {} and k = {}".format(n, k))

# Use sympy.euler() method 
nth_euler_poly = euler(n, k)  

print("The nth euler polynomial : {}".format(nth_euler_poly))  
```

**输出:**

```py
Value of n = 5 and k = x
The nth euler polynomial : x**5 - 5*x**4/2 + 5*x**2/2 - 1/2

```

**示例#3:**

```py
# import sympy 
from sympy import * n = 4
k = 3
print("Value of n = {} and k = {}".format(n, k))

# Use sympy.euler() method 
nth_euler_poly = euler(n, k)  

print("The nth euler polynomial value : {}".format(nth_euler_poly))  
```

**输出:**

```py
Value of n = 4 and k = 3
The nth euler polynomial value : 30

```