# Python 症状| sieve.mobiusrange()方法

> 原文:[https://www . geesforgeks . org/python-sympy-screen-mobiusrange-method/](https://www.geeksforgeeks.org/python-sympy-sieve-mobiusrange-method/)

借助**sympy . screen . mobiusrange()**方法，我们可以为给定范围**【a，b)** 生成[莫比乌斯数](https://en.wikipedia.org/wiki/M%C3%B6bius_function)。它返回一个类型生成器对象，该对象可以被转换为一个列表以供进一步操作。

> **语法:**screen . mobiusrange(a，b)
> **参数:**
> **a–**它表示范围的开始。它是包容的。
> **b–**表示范围的终点。它不具有包容性。
> **返回:**该方法返回一个类型生成器对象。

**示例#1:**

```
# import sympy 
from sympy import sieve

# Use sieve.mobiusrange() method 
mobius_gen = sieve.mobiusrange(1, 10) 
mobius_list = list(mobius_gen)

print("Mobius numbers for the range of numbers [1, 10) : {}".format(mobius_list))  
```

**输出:**

```
Mobius numbers for the range of numbers [1, 10) : [1, -1, -1, 0, -1, 1, -1, 0, 0]

```

**例 2:**

```
# import sympy 
from sympy import sieve

# Use sieve.mobiusrange() method 
mobius_gen = sieve.mobiusrange(8, 20) 
mobius_list = list(mobius_gen)

print("Mobius numbers for the range of numbers [8, 20) : {}".format(mobius_list))     
```

**输出:**

```
Mobius numbers for the range of numbers [8, 20) : [0, 0, 1, -1, 0, -1, 1, 1, 0, -1, 0, -1]

```