# Python | sympy.bell()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-bell-method/](https://www.geeksforgeeks.org/python-sympy-bell-method/)

借助 **sympy.bell()** 方法，我们可以在 sympy 中找到[贝尔数](http://mathworld.wolfram.com/BellNumber.html)和[贝尔多项式](http://mathworld.wolfram.com/BellPolynomial.html)。

### `bell(n) -`

> **语法:**铃(n)
> 
> **参数:**
> **n–**表示铃号的顺序。
> 
> **返回:**返回第 n <sup>个</sup>铃号。

**示例#1:**

```
# import sympy 
from sympy import * n = 5
print("Value of n = {}".format(n))

# Use sympy.bell() method 
nth_bell = bell(n)  

print("Value of nth bell number : {}".format(nth_bell))  
```

**输出:**

```
Value of n = 5
Value of nth bell number : 52

```

### 贝尔(n，k)–

> **语法:**贝尔(n，k)
> 
> **参数:**
> **n–**表示钟多项式的阶。
> **k–**表示贝尔多项式中的变量。
> 
> **返回:**返回贝尔多项式的表达式或其值。

**例 2:**

```
# import sympy 
from sympy import * n = 5
k = symbols('x')
print("Value of n = {} and k = {}".format(n, k))

# Use sympy.bell() method 
nth_bell_poly = bell(n, k)  

print("The nth bell polynomial : {}".format(nth_bell_poly))  
```

**输出:**

```
Value of n = 5 and k = x
The nth bell polynomial : x**5 + 10*x**4 + 25*x**3 + 15*x**2 + x

```

**示例#3:**

```
# import sympy 
from sympy import * n = 5
k = 3
print("Value of n = {} and k = {}".format(n, k))

# Use sympy.bell() method 
nth_bell_poly = bell(n, k)  

print("The nth bell polynomial value : {}".format(nth_bell_poly))  
```

**输出:**

```
Value of n = 5 and k = 3
The nth bell polynomial value : 1866

```

### bell(n，k，(x1，x2，x3，…)–

> **语法:** bell(n，k，(x1，x2，x3，…)
> 
> **参数:**
> **n–**表示第二类贝尔多项式的阶。
> **k–**它是第二类贝尔多项式中的一个参数。
> **(x1，x2，x3，…)–**表示变量符号的元组。
> 
> **返回:**返回第二类贝尔多项式。

**示例#4:**

```
# import sympy 
from sympy import * n = 5
k = 3
variables = symbols('x:6')[1:]
print("Value of n = {}, k = {} and variables = {}".format(n, k, variables))

# Use sympy.bell() method 
nth_bell_poly = bell(n, k, variables)  

print("The nth bell polynomial of second kind : {}".format(nth_bell_poly))  
```

**输出:**

```
Value of n = 5, k = 3 and variables = (x1, x2, x3, x4, x5)
The nth bell polynomial of second kind : 10*x1**2*x3 + 15*x1*x2**2

```