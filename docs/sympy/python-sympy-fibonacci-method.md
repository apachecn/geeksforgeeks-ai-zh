# Python | sympy.fibonacci()方法

> 原文:[https://www . geesforgeks . org/python-sympy-Fibonacci-method/](https://www.geeksforgeeks.org/python-sympy-fibonacci-method/)

借助 **sympy .斐波那契()**方法，我们可以在 sympy 中找到[斐波那契数和斐波那契多项式](https://en.wikipedia.org/wiki/Fibonacci_number)。

## `fibonacci(n) -`

斐波那契数是由初始项![F_0 = 0](img/2d9513ef2664a967de07205d6433a638.png "Rendered by QuickLaTeX.com")、![F_1 = 1](img/2686e5c01054797b7b1b6014d869a197.png "Rendered by QuickLaTeX.com")和两项递推关系![F_n = F_{n-1} + F_{n-2}](img/5d3dee64eb0f4f6bd2185452bdf5e943.png "Rendered by QuickLaTeX.com")定义的整数序列。

> **语法:**斐波那契(n)
> 
> **参数:**
> **n–**表示斐波那契数要计算到的数字。
> 
> **返回:**返回第 n 个<sup>斐波那契数。</sup>

**示例#1:**

```py
# import sympy 
from sympy import * 

n = 7
print("Value of n = {}".format(n))

# Use sympy.fibonacci() method 
nth_fibonacci = fibonacci(n)  

print("Value of nth fibonacci number : {}".format(nth_fibonacci))  
```

**输出:**

```py
Value of n = 7
Value of nth fibonacci number : 13

```

## `fibonacci(n, k) -`

斐波那契多项式由![F_1(k) = 1](img/648fe1d96ed1ec9d0b03693592c48fc4.png "Rendered by QuickLaTeX.com")、![F_2(k) = k](img/cb77d08bea8de1d65f710b96beb667a9.png "Rendered by QuickLaTeX.com")和![n > 2](img/0edf4aae5a6e711abdb9d0b6702a6f6a.png "Rendered by QuickLaTeX.com")的![F_n(k) = k*F_{n-1}(k) + F_{n-2}(k)](img/9b877e549f28cc1debf64f67b88204bf.png "Rendered by QuickLaTeX.com")定义。对于所有正整数![n](img/42ce0a847b20a2f8a781c8a50bdab975.png "Rendered by QuickLaTeX.com")、![F_n(1) = F_n](img/53d5335d8c836d4a4974c3f4aa50d643.png "Rendered by QuickLaTeX.com")。

> **语法:**斐波那契(n，k)
> 
> **参数:**
> **n–**表示第 n 个<sup>次</sup>斐波那契多项式。
> **k–**表示斐波那契多项式中的变量。
> 
> **返回:**返回 k，F <sub>n</sub> 中的第 n 个斐波那契多项式(k)

**例 2:**

```py
# import sympy 
from sympy import * 

n = 5
k = symbols('x')
print("Value of n = {} and k = {}".format(n, k))

# Use sympy.fibonacci() method 
nth_fibonacci_poly = fibonacci(n, k)  

print("The nth fibonacci polynomial : {}".format(nth_fibonacci_poly))  
```

**输出:**

```py
Value of n = 5 and k = x
The nth fibonacci polynomial : x**4 + 3*x**2 + 1

```

**示例#3:**

```py
# import sympy 
from sympy import * 

n = 6
k = 3
print("Value of n = {} and k = {}".format(n, k))

# Use sympy.fibonacci() method 
nth_fibonacci_poly = fibonacci(n, k)  

print("The nth fibonacci polynomial value : {}".format(nth_fibonacci_poly))  
```

**输出:**

```py
Value of n = 6 and k = 3
The nth fibonacci polynomial value : 360

```