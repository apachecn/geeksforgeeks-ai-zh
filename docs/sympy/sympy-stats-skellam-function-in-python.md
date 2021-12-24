# Python 中的 sympy . stats . skelem()函数

> 原文:[https://www . geesforgeks . org/sympy-stats-skelem-function-in-python/](https://www.geeksforgeeks.org/sympy-stats-skellam-function-in-python/)

借助**sympy . stats . Skellam()**方法，我们可以创建一个具有 skelem 分布的离散随机变量。

斯凯尔姆是两个统计上独立的随机变量 N1 和 N2 的 N1-N2 差的分布，每个都是泊松分布的，具有各自的期望值 mu1 和 mu2。

```
Syntax:  sympy.stats.Skellam(name, mu1, mu2)

Parameters:
 mu1: A non-negative value
 mu2:  A non-negative value

Returns: discrete random variable with a Skellam distribution.

```

**示例#1 :**

## 蟒蛇 3

```
# import sympy, Skellam, density, Symbol
from sympy.stats import Skellam, density
from sympy import Symbol

mu1 = Symbol("mu1", positive = True)
mu2 = Symbol("mu2", positive = True)

# using sympy.stats.Skellam() method
X = Skellam("x", mu1, mu2)
skeDist = density(X)(z)

print(skeDist)
```

**输出:**

```
(mu1/mu2)**(z/2)*exp(-mu1 - mu2)*besseli(z, 2*sqrt(mu1)*sqrt(mu2))

```

**例 2 :**

## 蟒蛇 3

```
# import sympy, Skellam, density
from sympy.stats import Skellam, density

# using sympy.stats.Skellam() method
X = Skellam("x", 1, 2)
skeDist = density(X)(3)

print(skeDist)
```

**输出:**

```
sqrt(2)*exp(-3)*besseli(3, 2*sqrt(2))/4

```