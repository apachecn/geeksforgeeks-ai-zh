# Python 中的 sympy.stats.Binomial()函数

> 原文:[https://www . geesforgeks . org/sympy-stats-二项式-python 中的函数/](https://www.geeksforgeeks.org/sympy-stats-binomial-function-in-python/)

借助 **sympy.stats.Binomial()** 方法，我们可以创建一个表示二项分布的有限随机变量。

二项式分布是实验或调查中重复多次的成功或失败结果的概率。

```
Syntax: sympy.stats.Binomial(name, n, p, succ=1, fail=0)

Parameters:
 name: distribution name
 n: Positive Integer, represents number of trials
 p: Rational Number between 0 and 1, represents probability of success
 succ: Represents event of success, by default is 1
 fail: Represents event of failure, by default is 0

```

**示例#1 :**

## 蟒蛇 3

```
# Import sympy, Binomial, density
from sympy.stats import Binomial, density

# Using sympy.stats.Binomial() method
X = Binomial('X', 4, 1 / 3)
binDist = density(X).dict

print(binDist)
```

**输出:**

```
{0: 16/81, 1: 32/81, 2: 8/27, 3: 8/81, 4: 1/81}

```

**例 2 :**

## 蟒蛇 3

```
# Import sympy, Binomial, density
from sympy.stats import Binomial, density

# Using sympy.stats.Binomial() method
X = Binomial('X', 4, 1 / 3, 1 / 2)
binDist = density(X).dict

print(binDist)
```

**输出:**

```
{0: 16/81, 1/2: 32/81, 2: 1/81, 3/2: 8/81, 1: 8/27}

```