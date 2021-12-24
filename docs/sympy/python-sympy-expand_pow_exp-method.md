# Python | sympy.expand_pow_exp()方法

> 原文:[https://www . geesforgeks . org/python-sympy-expand _ pow _ exp-method/](https://www.geeksforgeeks.org/python-sympy-expand_pow_exp-method/)

借助 **sympy.expand_pow_exp()** 方法，我们可以使用以下等式扩展数学表达式–

```py
 x<sup>(a+b)</sup> = x<sup>a</sup>.x<sup>b</sup>
```

> **语法:** expand_pow_exp(表达式)
> **参数:**
> **表达式**–是需要展开的数学表达式。
> 
> **返回:**返回对应于输入表达式的扩展数学表达式。

**例#1:**
在这个例子中我们可以看到，通过使用**sympy . exp _ pow _ exp()**方法，我们可以用幂展开一个数学表达式。

## 蟒蛇 3

```py
# import sympy
from sympy import * 

x, a, b = symbols('x a b')
expr = x**(a + b)

print("Before Expansion : {}".format(expr))

# Use sympy.expand_pow_exp() method
smpl = expand_pow_exp(expr) 

print("After Expansion : {}".format(smpl)) 
```

**输出:**

```py
Before Expansion : x**(a + b)
After Expansion : x**a*x**b

```

**例 2:**

## 蟒蛇 3

```py
# import sympy
from sympy import * 

x, a, b = symbols('x a b')
expr = x**(2 * a + 3 * b)

print("Before Expansion : {}".format(expr))

# Use sympy.expand_pow_exp() method
smpl = expand_pow_exp(expr) 

print("After Expansion : {}".format(smpl)) 
```

**输出:**

```py
Before Expansion : x**(2*a + 3*b)
After Expansion : x**(2*a)*x**(3*b)

```