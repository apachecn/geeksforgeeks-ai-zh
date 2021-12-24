# Python | sympy . smooth()方法

> 原文:[https://www . geesforgeks . org/python-sympy-smooth-method/](https://www.geeksforgeeks.org/python-sympy-smoothness-method/)

借助**sympy . smooth()**方法，我们可以求出给定数的光滑度和幂光滑度。一个数的光滑度是它的最大质因数，幂光滑度是它的最大除数。

> **句法:**
> 流畅度(n)
> 
> **参数:**
> **n–**表示计算平滑度和幂平滑度的数值。
> 
> **返回:**
> 返回给定数字的光滑度和幂光滑度的元组。

**示例#1:**

```
# import smoothness() method from sympy
from sympy.ntheory.factor_ import smoothness

n = 64

# Use smoothness() method 
smoothness_n, power_smoothness_n = smoothness(n) 

print("The smoothness and power-smoothness of {} is {} and {} respectively".
      format(n, smoothness_n, power_smoothness_n))
```

**输出:**

```
The smoothness and power-smoothness of 64 is 2 and 64 respectively

```

**例 2:**

```
from sympy.ntheory.factor_ import smoothness

n = 2**4 * 13

# Use smoothness() method 
smoothness_n, power_smoothness_n = smoothness(n) 

print("The smoothness and power-smoothness of {} is {} and {} respectively".
      format(n, smoothness_n, power_smoothness_n))
```

**输出:**

```
The smoothness and power-smoothness of 208 is 13 and 16 respectively

```