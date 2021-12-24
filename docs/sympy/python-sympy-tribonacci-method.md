# Python | sympy.tribonacci()方法

> 原文:[https://www . geesforgeks . org/python-sympy-tribonacci-method/](https://www.geeksforgeeks.org/python-sympy-tribonacci-method/)

借助 **sympy.tribonacci()** 方法，我们可以在 sympy 中找到 [tribonacci 数和 Tribonacci 多项式](https://en.wikipedia.org/wiki/Generalizations_of_Fibonacci_numbers#Tribonacci_numbers)。

## `tribonacci(n) -`

Tribonacci 数是由初始项![T_0 = 0](img/e7a17ef8521d8d7f1a9ac05d74b67ff7.png "Rendered by QuickLaTeX.com")、![T_1 = 1](img/f540aaa14f83b65246cb3c235945c4d4.png "Rendered by QuickLaTeX.com")、![T_2 = 1](img/4f383c92c2df1dd40be3240451cb1f8b.png "Rendered by QuickLaTeX.com")和三项递推关系![T_n = T_{n-1} + T_{n-2} + T_{n-3}](img/8332cb02cc5f64a7b69b75820616be3b.png "Rendered by QuickLaTeX.com")定义的整数序列。

> **语法:** tribonacci(n)
> 
> **参数:**
> **n–**它表示要计算的 Tribonacci 数。
> 
> **返回:**返回第 n 个<sup>号</sup>摩擦号。

**示例#1:**

```py
# import sympy 
from sympy import * 

n = 7
print("Value of n = {}".format(n))

# Use sympy.tribonacci() method 
nth_tribonacci = tribonacci(n)  

print("Value of nth tribonacci number : {}".format(nth_tribonacci))  
```

**输出:**

```py
Value of n = 7
Value of nth tribonacci number : 24

```

## `tribonacci(n, k) -`

对于![n > 2](img/0edf4aae5a6e711abdb9d0b6702a6f6a.png "Rendered by QuickLaTeX.com")，特里博纳西多项式由![T_0(k) = 0](img/b95f4d301043fcbae3c7439b3c821fa3.png "Rendered by QuickLaTeX.com")、![T_1(k) = 1](img/eef3c6986bb883d3616d0c03c07d30a1.png "Rendered by QuickLaTeX.com")、![T_2(k) = k^2](img/201bd5c7b889a29398485f02a4bab2c5.png "Rendered by QuickLaTeX.com")和![T_n(k) = k^2 T_{n-1}(k) + k T_{n-2}(k) + T_{n-3}(k)](img/627cb7c258646c60a12980cde335a397.png "Rendered by QuickLaTeX.com")定义。对于所有正整数![n](img/42ce0a847b20a2f8a781c8a50bdab975.png "Rendered by QuickLaTeX.com")、![T_n(1) = T_n](img/c2ae137b6b8294d0394e176218893c95.png "Rendered by QuickLaTeX.com")。

> **语法:** tribonacci(n，k)
> 
> **参数:**
> **n–**表示第 n 个<sup>次</sup>摩擦多项式。
> **k–**表示 Tribonacci 多项式中的变量。
> 
> **返回:**返回 k，T <sub>n</sub> (k)中的第 n 个 Tribonacci 多项式

**例 2:**

```py
# import sympy 
from sympy import * 

n = 5
k = symbols('x')
print("Value of n = {} and k = {}".format(n, k))

# Use sympy.tribonacci() method 
nth_tribonacci_poly = tribonacci(n, k)  

print("The nth tribonacci polynomial : {}".format(nth_tribonacci_poly))  
```

**输出:**

```py
Value of n = 5 and k = x
The nth tribonacci polynomial : x**8 + 3*x**5 + 3*x**2

```

**示例#3:**

```py
# import sympy 
from sympy import * 

n = 6
k = 3
print("Value of n = {} and k = {}".format(n, k))

# Use sympy.tribonacci() method 
nth_tribonacci_poly = tribonacci(n, k)  

print("The nth tribonacci polynomial value : {}".format(nth_tribonacci_poly))  
```

**输出:**

```py
Value of n = 6 and k = 3
The nth tribonacci polynomial value : 68289

```